<h1 style="text-align: center;"> Functions </h1>

## What are functions? 

A function is a block of reusable code that performs a specific task. It can take in arguments (also called parameters), process those inputs, and may or may not return a result.

Here's breakdown:

- Arguments: These are the inputs you provide to the function. A function can take zero or more arguments.

- Return value: A function may return a result after performing its task. If it doesn’t return anything explicitly, it typically returns None (in Python) or an equivalent value in other languages.

- Reusable: Functions allow you to reuse code without rewriting it each time you need to perform the same operation.

**def** - key word to identity function

```
def functionName(Argument/Parameter):
"
Doc string
"
Logic

return Something or nothing 

functionName() --> Calling a function
```
```
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
- Parameter : When creating the function 
- Argument : While using the function 

## Types of Arguments

- Default Argument
- Positional Argument : *Argument follows parameter order*
- Keyword Argument 
```
# Default Argument
def power(a=1, b=1):
    return a**b

power(3)

--output--
3
```
## Keyword Argument

Specify parameters when positions are non-known

```
def power(a=1,b=1):
    return a**b

power(b=3, a=2)

--output--
8
```
# *Args and *Kwargs

`*Args and *Kwargs` are special python keywords that are used to pass variable length of arguments to a function. 

## *Args

Allow us to pass a variable number of non-keyword arguments to a function. 

```
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

Kwargs allows us to pass any number of keyword arguments.

Keyword arguments mean that they contain a key-value pair, like a python dictionary. 

## Points to remember

- Order of the argument matters (`normal` -> `*args` -> `**kwargs`)
- The words `args` and `kwargs` are only a convention, you can use any name of your choice

## Documentation of a function 

```
function.__doc__
```
