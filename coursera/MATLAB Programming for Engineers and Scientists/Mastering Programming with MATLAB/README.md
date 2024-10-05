
## Module 2

### Variable Number of Arguments

![fprintf](fprintf.png)

```MATLAB
function index = find_first(v,e)
    if nargin == 0
        error('At least one argument is required')
    elseif nargin == 1
        e = 0;
    end
    index = 0;
    indices = find(v == e);
    if ~isempty(indices)
        index = indices(1);
    end
end
```
```MATLAB
>> rng(0); w = randi([-3, 3], 1, 12)
>> find_first(w,1)
>> find_first(w,2)
>> find_first(w,12)
>> find_first(w,0)
>> find_first(w)
```

```MATLAB
function print_all(varargin)
    for ii = 1:nargin
        fprintf('Here is input argument number %d: %d\n', ii, varargin{ii})
    end
end
```

```MATLAB
>> print_all(pi)
>> print_all(7, -3)
>> print_all(8, 0, 4, 18234, 5.67)
>> sprintf('the first three positive integers are %d, %d, and %d',1,2,3)
```

```MATLAB
function out = print_num(format,varargin)
    out = '';
    argindex = 1;
    skip = false;
    for ii = 1:length(format)
        if skip
            skip = false;
        else
            if format(ii) ~= '%'
                out(end+1) = format(ii);
            else
                if ii+1 > length(format)
                    break;
                end
                if format(ii+1) == '%'
                    out(end+1) = '%';
                else
                    if argindex >= nargin
                        error('not enough input arguments');
                    end
                    out = [out num2str(varargin{argindex},format(ii:ii+1))];
                    argindex = argindex + 1;
                end
                skip = true;
            end
        end
    end
end
```

```MATLAB
>> print_num('the first three positive integers are %d, %d, and %d',1,2,3)
>> pct = 20; a = 934.4; print_num('%d%% of %f is %f', pct, a, a*pct/100)
>> print_num('let us make an error: %d', 1, 2)
>> print_num('let us make another error: %d and %f', 1) % gives error
```

```MATLAB
function varargout = distribute(v)
    for ii = 1:length(v)
        varargout{ii} = v(ii);
    end
end
```

```MATLAB
>> [a, b, c] = distribute([14, -pi, 0])
>> [a, b] = distribute([14, -pi, 0])
>> [a, b, c, d] = distribute([14, 15, 16]) % gives error
```

#### Problem 1: Name-value Pairs

Name-value pairs are frequently used in programming. For our purposes here, a name-value pair consists of a name (a char vector) and a value that can be of any data type. Write a function called name_value_pairs that has a variable number of input arguments representing name-value pairs. Naturally, they come in pairs: the first is the name, the next is the value. This means that the function must be called with an even number of actual input arguments. The function returns a single cell array which has exactly two columns: the first column contains the names, while the second column contains the values. If the function is called with no input arguments, or it is called with an odd number of inputs or if a name is not of char type, the function returns an empty cell array. Here is an example run:


```MATLAB
>> db = name_value_pairs('name','John Smith','age',32,'children',{'Joe' 'Jill'})
db =
  3x2 cell array
    {'name'    }    {'John Smith'}
    {'age'     }    {[        32]}
    {'children'}    {1x2 cell    }
```

```MATLAB
function db = name_value_pairs(varargin)
    if nargin == 0 || rem(nargin, 2) == 1
        db = {};
        return
    end
    jj = 1;
    for ii = 1:2:nargin
        if ischar(varargin{ii})
            db{jj,1} = varargin{ii};
            db{jj,2} = varargin{ii + 1};
            jj = jj + 1;
        else
            db = {};
            break;
        end
    end
end
```

```MATLAB
function store = sol_name_value_pairs(varargin)
    % Initialize an empty cell array
    store = {};
    % If the input does not come in pairs (remainder = 1), return
    if rem(length(varargin),2)
        return;
    end
    
    for ii = 1:floor(length(varargin)/2)
        % The Name part must be a char. If not, return an empty cell
        if ~ischar(varargin{2*ii-1})
            store = {};
            return;
        end
        store{ii,1} = varargin{2*ii-1};
        store{ii,2} = varargin{2*ii};
    end
end
```

#### Problem 2: Data Entry

In a voting center, the voters are required to give their names and ID numbers to the voting staff before going into the voting room. Write a function called voters to record the incoming voters' information. The function should take an unspecified number of inputs, but the first input will be the current database. The rest of the arguments must come in the order of name, a string or char array, and ID, an integer or integer-valued double. If there is at least one ocurrence of no ID number after a name, or the data types are not what's required, return the original database. The function should return a struct array containing Name (a string) and ID (a double) fields as shown below.

```MATLAB
>> database = voters([], 'Brandon', 12356)
database = 
  struct with fields:
    Name: "Brandon"
      ID: 12356

>> database = voters(database, "Mike", 9876, 'Akos', 112233)
database = 
  1x3 struct array with fields:
    Name
    ID

>> database(end)
ans = 
  struct with fields:
    Name: "Akos"
      ID: 112233
```

However, if there is an illegal call, the database should not change:

```MATLAB
>> database
database = 
  1x3 struct array with fields:
    Name
    ID

>> database = voters(database, 'Student', 99999, "No ID")
database = 
  1x3 struct array with fields:
    Name
    ID
```

```MATLAB
function db = voters(database, varargin)
    if isempty(database)
        db = struct('Name', {}, 'ID', {});
    end
    if rem(length(varargin),2) == 1
        db = database;
        return;
    end
    arguments_length = length(varargin)/2;
    for ii = 1:arguments_length
        jj = 2 * ii;
        if (ischar(varargin{jj-1}) || isstring(varargin{jj-1})) && isa(varargin{jj},'double') && (fix(varargin{jj})==(varargin{jj}))
            db(ii).Name = string(varargin{jj-1});
            db(ii).ID = double(varargin{jj});
        else
            db = database;
            return;
        end
    end
    db = [database db];
end
```

```MATLAB
function database = sol_voters(database,varargin)
    % Get the length of the input database
    count = length(database);
    
    % Create a copy of the database. This will be the new database if input
    % is valid
    tmp = database;
    
    % Names and IDs come in pairs. Increment loop counter by 2
    for ii = 1:2:length(varargin)
        % Make sure the Name is a char or string
        if ischar(varargin{ii}) || isstring(varargin{ii})
            count = count + 1;
            tmp(count).Name = string(varargin{ii});
            % Make sure there is a valid ID
            if ii+1 <= length(varargin) && isnumeric(varargin{ii+1}) && round(varargin{ii+1}) == varargin{ii+1}
                tmp(count).ID = varargin{ii+1};
            else
                % Not valid input. Return original database
                return;
            end
        else
            % Not valid input. Return orginal database
            return;
        end
    end
    % All inputs valid. Update database.
    database = tmp;
end
```