<h1 style="text-align: center;"> Loops and Functions</h1>

## What are loops? 

Loops are a fundamental concept in programming that allow you to `repeat a block of code multiple times`.

### Types of Loops

1. **For Loop**:
    - Used to iterate over a sequence (list, tuple, dictionary, string, or range).
    - Example:

        ```python 
        for i in range(5):
            print(i)  # Output: 0, 1, 2, 3, 4
        ```
2. **While Loop**:

    - Repeats a block of code as long as a condition is `True`      .
    - Example:
  
    ```python 
    i = 0
    while i < 5:
        print(i)
        i += 1  # Increment to avoid infinite loop
    ```

### Key Concepts

1. **Nested Loops**:

    - Loops inside another loop.
    - Example:
    ```python 
    for i in range(3):
        for j in range(2):
            print(f"i={i}, j={j}")
    ```
2. **Break and Continue**:

    - `break`: Exit the loop prematurely.
    - `continue`: Skip the current iteration and move to the next.
    - Example

    ```python 
    for i in range(5):
        if i == 3:
            break  # Stop the loop when i equals 3
        print(i)
    ```
3. **Else with Loops**:

    - The `else block` runs after the loop finishes, unless interrupted by a break.
    - Example:
    ```python 
    for i in range(3):
        print(i)
    else:
        print("Loop completed!")  # Will execute because no break occurred
    ```
---

## What are functions? 

A function is a block of `reusable code` that performs a `specific task`. It can take in arguments (also called `parameters`), process those inputs, and `may or may not return a result`.

Here's breakdown:

- `Arguments`: These are the inputs you provide to the function. A function can take `zero or more arguments`.

- `Return value`: A function may return a result after performing its task. If it doesn’t return anything explicitly, it typically returns `None` (in Python) or an equivalent value in other languages.

- `Reusable`: Functions allow you to `reuse code without rewriting it each time` you need to perform the same operation.

**def** - key word to identity function

```python
def functionName(Argument/Parameter):
"
Doc string
"
Logic

return Something or nothing 

functionName() --> Calling a function
```
```python
def is_even(num):
    """
    This function returns if a given number is odd or even
    Input - any valid integer
    output - Odd/even
    Created on - 9/29/2024
    """

    if num % 2==0:
        return "Even"
    else:
        return "Even"
    
is_even(10)

--output--
'Even'
```
# 2 Point of Views
- Person writing the code (*Must be careful of all test-cases*)
- Person using the code

## Parameter vs Argument
- `Parameter` : When creating the function 
- `Argument` : While using the function 

## Types of Arguments

- Default Argument
- Positional Argument : *Argument follows parameter order*
- Keyword Argument 
```python
# Default Argument
def power(a=1, b=1):
    return a**b

power(3)

--output--
3
```
## Keyword Argument

Specify parameters when positions are non-known

```python
def power(a=1,b=1):
    return a**b

power(b=3, a=2)

--output--
8
```
# *Args and *Kwargs

`*Args and *Kwargs` are special symbols used in function definitions to allow for flexible and dynamic handling of arguments. 

## *Args

- `Purpose` : Allows a function to accept a variable number of positional arguments (arguments without keywords).
- `Syntax` : Use a single asterisk (*) followed by a variable name (commonly args, but you can name it anything).
- `Behavior` : Captures extra positional arguments passed to the function and stores them in a tuple.


```python
def multiply(a,b,c):
    return a*b*c

def multiple(*args):
    product = 1

    for i in arges:
        product = product * i
    return product

--output--
multiple(1,5,6,7,10)
```

*Args will store the values in `tuples`

## **Kwargs 

- `Purpose`: Allows a function to accept a variable number of keyword arguments (arguments with names).
- `Syntax`: Use a double asterisk (**) followed by a variable name (commonly kwargs, but you can name it anything).
- `Behavior`: Captures extra keyword arguments passed to the function and stores them in a dictionary. 

```python
def display_info(**kwargs):
    for key, value in kwargs.items():
        print(f"{key}: {value}")

display_info(name="Alice", age=30, city="New York")

--output--
name: Alice
age: 30
city: New York
```

## Points to remember

- Order of the argument matters (`normal` -> `*args` -> `default arguments` -> `**kwargs`)
- The words `args` and `kwargs` are only a convention, you can use any name of your choice

## Documentation of a function 

```
function.__doc__
```

## How functions are executed in memory?

Function acts as a small independent program in memory. 
```python
def is_even(x):
    """
    The purpose of this function is to 
    find whether a number is even or odd
    """

    if x %2 ==0:
        print('Even')
    elif x%2 !=0:
        print('Odd')
    else:
        print('Not proper input')
```
## Without return statment

Function with no return values will return `NONE`

```python
# without return statment

L = [1,2,3]
print(L.append(4))

--output--
None
```
## Key Differences Between Return and Print

### Return Value:

- return gives a value back to the caller, allowing the result to be used elsewhere.
- print() only outputs something to the console but returns None.

Use:

- return is used to pass data out of a function.
- print() is used to display data to the user.

### Function Flow:

- return ends the function's execution immediately.
- print() does not affect the flow of execution.

## Variable Scope
- `Global Variable` : Part of main program
- `Local Variable` : Part of function

Local variables can use `Global variables`, but the `opposite` is not the same. 

Global variable and local variable can have same names.

## Functions are 1st Class Citizen 

first class citizens are treated the same way as a data types where any operation can be applied  

- Functions can be reassign 
- Functions can be deleted 
- Functions can be stored in a list, tuple, dict, etc
- Functions are not mutable (set test)

```python
def square(x):
    return x**2

x = square 
x(3)

--output--
9
```

## Benefits of using a Function 

- Code Modularity
- Code Readibility 
- Code Reusability 

## Lambda Function 

A lambda function in Python is a small, anonymous function that is defined without a name using the lambda keyword. It is typically used for short, simple operations.

    lambda arguments: expression
    
    lambda a,b : a + b 

```python
x = lambda x: x**2

x(2)

--output--
4
```

### Difference between lambda and normal funciton
- No name
- Lambda has no return value
- lambda is written in 1 line
- not reusable 

### Why use lambda funciton?
They are used with High-order-function 

### Higher Order Function 

A type of function that either returns a function or recieve a function as an input

- Map
- Reduce
- Filter



