# Python Essentials


## 4.1.1.1 Functions


## 4.1.1.4 Writing functions

### Your first function
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