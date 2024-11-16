# Decorator & Namespaces

## Namespaces

A **namespace** is a space that holds names (identifiers). Programs use namespaces to organize and manage variable names across different scopes.

**There are 4 types of namespaces**:
- **Builtin Namespace**: Holds built-in functions and exceptions, like `print`, `len`, etc.
- **Global Namespace**: Holds global variables and functions, usually at the module level.
- **Enclosing Namespace**: Holds variables defined in an outer function, accessible within nested functions.
- **Local Namespace**: Holds local variables defined within a function.

### Scope and LEGB Rule

A **scope** is a textual region of a Python program where a namespace is directly accessible.

The interpreter searches for a name from the innermost to the outermost scope using the **LEGB rule**:

- **L (Local)**: The innermost scope, typically the function you’re currently in.
- **E (Enclosing)**: The scope of any enclosing functions, particularly relevant in nested functions.
- **G (Global)**: The module-level scope; variables defined outside of all functions.
- **B (Builtin)**: The outermost scope, containing built-in functions and names.

### Example of LEGB Rule

```python
# Global scope
x = "global"

def outer():
    # Enclosing scope
    x = "enclosing"

    def inner():
        # Local scope
        x = "local"
        print("Inside inner:", x)  # Prints 'local'

    inner()
    print("Inside outer:", x)      # Prints 'enclosing'

outer()
print("Outside all functions:", x) # Prints 'global'
```

## Purpose of `nonlocal`

The `nonlocal` keyword is used to declare a variable in an **enclosing scope** (not global) as accessible and modifiable within a nested function. It’s helpful when you have nested functions and want to modify a variable from an outer (enclosing) function without making it global.

In Python, without `nonlocal`, variables in the enclosing scope are read-only in nested functions. By using `nonlocal`, you tell Python to access and update the variable in the closest enclosing scope.

### How `nonlocal` Works with LEGB Rule

- **L (Local)**: If a variable is assigned within a function, it is local to that function.
- **E (Enclosing)**: The `nonlocal` keyword allows access to the nearest enclosing (non-global) variable, enabling modification of a variable defined in an outer function.
- **G (Global)**: If a variable is declared as `global`, it affects the global scope.
- **B (Builtin)**: Built-in scope remains unaffected by `nonlocal`.

### Example of `nonlocal`

Consider this example, where `nonlocal` is used to modify a variable in an enclosing scope:

```python
def outer_function():
    x = "outer value"

    def inner_function():
        nonlocal x
        x = "modified by inner"
        print("Inside inner_function:", x)  # Prints 'modified by inner'

    inner_function()
    print("Inside outer_function:", x)      # Prints 'modified by inner'

outer_function()
```

# Decorators in Python

## What is a Decorator?

A **decorator** is a function in Python that takes another function as an argument, adds some functionality to it, and returns a new function with the added functionality. Decorators allow you to "wrap" functions or methods, modifying their behavior without changing their code.

Decorators are commonly used in Python for logging, access control, memoization, and other reusable functions.

### Syntax of a Decorator

A decorator is applied to a function using the `@decorator_name` syntax, placed directly above the function definition.

```python
@decorator_name
def function_name():
    # Function code
    pass
```

### How decorator works?

```python
def my_decorator(func):
    def wrapper():
        print("Something is happening before the function is called.")
        func()
        print("Something is happening after the function is called.")
    return wrapper

@my_decorator
def say_hello():
    print("Hello!")

say_hello()
```
