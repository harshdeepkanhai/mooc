

















## Module 5

### Introduction to Programmer's Toolbox

- polymorphism
![polymorphism](polymorphism.png)


### Matrix Building

```MATLAB
>>zeros(5,6)
>>ones(4,2)
>>5 + ones(4,2)
>>zeros(4)
>>diag([7 3 9 1])
>>rand
>>rand(3,4)
>>rand(5)
>>1 + rand(5,4) * 10
>>fix(1 + rand(5,4) * 10)
>>randi(10,5,4)
>>randi(20, 5)
>>randi([5 10],2, 3)
>>randn(5)
>>r = randn(1, 1000000);
>>hist(r,100)
```
![random sequence initialization](rsi.png)

```MATLAB
>>rng(0);
>>rand(1,3)
>>rng(1)
>>[rand, randnm, randi(10)]
>>rng('shuffle');[rand, randnm, randi(10)]
```

### Input / Output

```MATLAB
>>edit one_more
```

```MATLAB
function a = one_more
x = input('Gimme a number, buddy: ');
a = x + 1;
```

```MATLAB
>>fprintf('This concludes lesson 3\n')
```

```MATLAB
function check_out(n, price)
    total = n * price;
    fprintf('%d items at %.2f each\nTotal = $%5.2f\n',n,price,total);
end
```

`\` and `%` are called escape character.

```MATLAB

fprintf('12.5%% of 1234 equals %.3f\n', 0.125*1234)
fprintf('This is a backslash character: \\\n')
fprintf('How about a single quote ('')?\n')
```

```MATLAB

fprintf('%d lb butter, %d tbsp cocoa, %d cps flour, and %d cps sugar\n', 1, 8, 4, 4)
```

If we miss a value in `fprintf` less the the `%` sign it will print till the `%` sign

If we have extra value than the `%` sign it will repeat from the beginning like circular.

```MATLAB
>>fprintf('%4.1f\n', [1 2 3 4 5 6]);
```

### Plotting

```MATLAB
>>a= [1:10].^2
>>plot(a)
>>figure(2);
>>a= [-10:10].^2
>>plot(a)
>>t=-10:10
>>b=t.^2
>>figure
>>plot(t,b);
```

```MATLAB
>>x1 = 0:0.1:2*pi; y1=sin(x1);
>>x2 = pi/2:0.1:3*pi; y2=cos(x2);
>>plot(x1,y1,x2,y2)
>>figure
>>plot(x1,y1,'r',x2,y2,'k:')
```

```MATLAB
>>figure(1)
>>plot(t,b,'m--o')
```

```MATLAB
>>figure(2)
>>plot(x1, y1,'r')
>>hold on
>>plot(x2, y2,'k:')
>>hold off
>>plot(x1,y1,'g*')
>>figure(3)
>>grid
>>title('A sine Plot and a cosine Plot');
>>xlabel('The argument of sine and cosine')
>>ylabel('The value for sine or cosine')
>>legend('sine','cosine')
>>axis([-2 12 -1.5 1.5])\
>>close(4)
>>close all
```

### Debugging

![Debugging](debugging.png)