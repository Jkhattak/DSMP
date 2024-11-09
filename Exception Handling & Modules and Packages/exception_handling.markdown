# Exception Handling & Modules and Packages

There are two stages where error may happen in program 

- During Compilation &rightarrow; Syntax Error
- During exectution &rightarrow; Exception 

## Syntax Error
- Something in the program is not written according to the program
- Error is raised by the interpreter/compiler
- You can solve it by rectifying the program 

`print 'hello world' &rightarrow; will result in `syntax error`

### Other examples of syntax error
- Leaving symbols like colon, brackets
- Misspelling a keyword
- Incorrect indentation
- Empty if/else/loops/class/function
  
# Common Python Errors

## 1. `IndexError`
- **Definition**: Raised when trying to access an index that is out of range in a list or other indexed collection.
- **Example**:
    ```python
    my_list = [1, 2, 3]
    print(my_list[3])  # IndexError: list index out of range
    ```

## 2. `ModuleNotFoundError`
- **Definition**: Raised when Python cannot find a module specified in an import statement.
- **Example**:
    ```python
    import non_existent_module  # ModuleNotFoundError: No module named 'non_existent_module'
    ```

## 3. `KeyError`
- **Definition**: Raised when trying to access a dictionary key that does not exist.
- **Example**:
    ```python
    data = {"name": "Alice"}
    print(data["age"])  # KeyError: 'age'
    ```

## 4. `TypeError`
- **Definition**: Raised when an operation is performed on an inappropriate data type.
- **Example**:
    ```python
    result = "2" + 3  # TypeError: can only concatenate str (not "int") to str
    ```

## 5. `ValueError`
- **Definition**: Raised when a function receives an argument of the correct type but with an invalid value.
- **Example**:
    ```python
    number = int("hello")  # ValueError: invalid literal for int() with base 10: 'hello'
    ```

## 6. `NameError`
- **Definition**: Raised when a local or global name is not found.
- **Example**:
    ```python
    print(age)  # NameError: name 'age' is not defined
    ```

## 7. `AttributeError`
- **Definition**: Raised when an attribute reference or assignment fails.
- **Example**:
    ```python
    my_string = "hello"
    my_string.append("!")  # AttributeError: 'str' object has no attribute 'append'
    ```

---

# Exception
If things go wrong during the execution of the program (runtime). It generally happens when something unforeseen has happened. 

- Exceptions are raised by python runtime 
- You have to takle is on the fly 

**Examples**
- Memory overflow
- Divide by 0 &rightarrow; logical error
- Database error


## Why Exception Handling is Important

1. **Prevents Program Crashes**  
   Unhandled exceptions can terminate a program unexpectedly, making it appear unreliable or buggy. Handling exceptions allows the program to continue running or terminate gracefully.

2. **Improves User Experience**  
   By handling exceptions, you can provide helpful error messages, guiding the user rather than displaying a confusing traceback.

3. **Enhances Code Readability and Maintainability**  
   Handling exceptions helps keep the main logic clean, organized, and focused, as potential errors are managed in a structured way.

4. **Supports Debugging and Troubleshooting**  
   With exception handling, you can log errors or provide specific details about what went wrong, making it easier to troubleshoot and debug.

5. **Promotes Robustness and Reliability**  
   Properly handled exceptions lead to a more reliable codebase, reducing the likelihood of unforeseen issues that could disrupt the program.

---

## How to Handle Exceptions in Python

Python provides a `try-except` block to handle exceptions. This structure allows you to catch and respond to errors gracefully.

### Basic Syntax

```python
try:
    # Code that might raise an exception
    result = 10 / 0
except ZeroDivisionError:
    # Code to handle the exception
    print("Cannot divide by zero!")
```

```python
try:
    with open('sample.txt', 'r') as f:
        print(f.read())
except:
    print('File not found')
```

### Using a Generic Exception Handler

```python
try:
    number = int(input("Enter a number: "))
    result = 10 / number
except ValueError:
    print("Invalid input! Please enter a number.")
except ZeroDivisionError:
    print("Cannot divide by zero!")
except Exception as e:
    print("An unexpected error occurred:", e)
```

### Else statement 


```python
try:
    f = open('sample.txt', 'r')
except:
    print("file not found")
else:
    print(f.read())
```

### Finally Statement 

```python
# finally statement
try:
    f = open('sample.txt', 'r')
except:
    print("file not found")
else:
    print(f.read())
finally:
    print("This will print")

```

### Python Exception Handling Flow with `try`, `except`, `else`, and `finally`

The `try`, `except`, `else`, and `finally` blocks allow you to handle exceptions effectively in Python. Here’s a flowchart that shows the logic of each block:

```mermaid
flowchart TD
    A[Start] --> B[try block]
    B -->|No Exception| C[else block]
    B -->|Exception Raised| D[except block]
    C --> E[finally block]
    D --> E
    E --> F[End]
```




