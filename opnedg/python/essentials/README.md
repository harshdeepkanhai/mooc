# Python Essentials


### 4.1.1.1 Functions


### 4.1.1.4 Writing functions

#### Your first function
How do you make such a function?

You need to define it. The word define is significant here.

This is what the simplest function definition looks like:

```python
def function_name():
    function_body
```
- It always starts with the **keyword** `def` (for define)
- next after `def` goes the **name of the function** (the rules for naming functions are exactly the same as for naming variables)
- after the function name, there's a place for a pair of **parentheses** (they contain nothing here, but that will change soon)
- the line has to be ended with a **colon**
- the line directly after def begins the **function body** ‒ a couple (at least one) of necessarily **nested instructions**, which will be executed every time the function is invoked; note: the **function ends where the nesting ends**, so you have to be careful.

We're ready to define our **prompting** function. We'll name it `message` ‒ here it is:

```python
def message():
    print("Enter a value: ")

```


The function is extremely simple, but fully **usable**. We've named it `message`, but you can label it according to your taste. Let's use it.

Our code contains the function definition now:

```python
def message():
    print("Enter a value: ")

print("We start here.")
print("We end here.")

```

Note: we don't use the function at all ‒ there's no **invocation** of it inside the code.

When you run it, you see the following output:

```python
We start here.
We end here.
```
This means that Python reads the function's definitions and remembers them, but won't launch any of them without your permission.

---

We've modified the code now ‒ we've inserted the **function's invocation** between the start and end messages:

```python
def message():
    print("Enter a value: ")

print("We start here.")
message()
print("We end here.")

```

The output looks different now:

```python
We start here.
Enter a value: 
We end here.
```

### 4.1.1.5 Functions

#### How functions work
Look at the picture below:
![function](https://edube.org/uploads/media/default/0001/01/f3a3fa6991f0ecb817a2a09c1aac0b45dba5579a.png)



### PE1 -- Module 4 Quiz

- A function definition starts with the keyword:
    - `function`
    - `fun`
    - `def`

    **Ans**: `def`

- A function definition:
    - cannot be placed among other code
    - may be placed anywhere inside the code after the first invocation
    - must be placed before the first invocation

    **Ans**: must be placed before the first invocation

- A function parameter is a kind of variable accessible:
    - only inside the function
    - only after the function definition's completion
    - anywhere in the code

    **Ans**: only inside the function

- A way of passing arguments in which  the order of  the arguments determines the initial parameter's value is referred to as:
    - positional
    - ordered
    - sequential

    **Ans**: positional

- Which of the following statements are true ? (Select two answers)
    - The `return` keyword may cause the function to return a value
    - The `return` keyword forces the function's execution to terminate
    - The `return` keyword forces the function to restart its execution

    **Ans**: The `return` keyword may cause the function to return a value, The `return` keyword forces the function's execution to terminate

- The `None` keyword designates:
    - an empty instruction
    - a `None` value
    - a function which doesn't return a value

    **Ans**: a `None` value

- A variable defined outside a function:
    - may not be accessed in any way inside the function
    - may be read, but not written (something more is needed to do so)
    - may be freely accessed inside the function

    **Ans**: may be read, but not written (something more is needed to do so)

- If a list is passed into a function as an argument, deleting any of its elements inside the function using the `del` instruction:
    - will cause a runtime error
    - will not affect the argument
    - will affect the argument

    **Ans**: will affect the argument

- What is the output of the following snippet ?
    ```python
    def fun(in=2, out=3):
        return in * out

    print(fun(3))
    ```
    - `6`
    - the snippet is errorneous (invalid syntax)
    - `9`

    **Ans**: the snippet is errorneous (invalid syntax)

- What is the output of the following snippet ?
    ```python
    tup = (1, ) + (1, )
    tup = tup + tup
    print(len(tup))
    ```
    - `4`
    - `2`
    - the snippet is errorneous (invalid syntax)

    **Ans**: `4`

- What is the output of the following program if the user enter `kangaroo` at the first prompt and `0` at the second prompt?
    ```python
    try:
        first_prompt = input("Enter the first value: ")
        a = len(first_prompt)
        second_prompt = input("Enter the second value: ")
        b = len(second_prompt) * 2
        print(a/b)
    except ZeroDivisionError:
        print("Do not divide by zero!")
    except ValueError:
        print("Wrong value.")
    except:
        print("Error.Error.Error.")
    ```
    - `Do not divide by zero!`
    - `Error.Error.Error.`
    - `4.0`
    - `Wrong value.`

    **Ans**: `4.0`

- What is the expected behavior of the following program if the user enters `0` ?
    ```python
    value = input("Enter a value: ")
    print(10/value)
    ```
    - The program will raise the `TypeError` exception.
    - The program will output `0` to the console.
    - The program will raise the `ValueError` exception.
    - The program will raise the `ZeroDivisionError` exception.

    **Ans**: The program will raise the `TypeError` exception.