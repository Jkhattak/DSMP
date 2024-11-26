# Objects 

## What is an object?

In Python, **everything is an object**. But what does this mean? Let’s break it down.

When you create a variable, Python doesn’t just store a value—it creates an object in memory to represent that value. This **object** has:

- A unique memory address (its identity).
- A type that defines its behavior (e.g., `str, int, list`).
- The value of the object itself.

For example, consider the statement:
```python
h = "hello world"
```
## What Happens in Memory?

- **Creating the Object:**
    - Python creates an object in heap memory to store the string `"hello world"`.
    - This object includes metadata:
        - Type: `str` (string).
        - Value: `"hello world"`.
        - Reference Count: Starts at 1 (for the variable `h`).

-   **Assigning the Variable:**
    - The variable `h` is created in stack memory and stores a reference (or pointer) to the memory address of the object.

- **Reusing Objects:**
  - If you create another variable with the same value, like:
    ```python
    a = "hello world"
    ```

    Python checks whether an object with this value already exists. Since strings are immutable and "hello world" is already stored, Python assigns a the same memory address as h. This is called object interning or string interning, and it optimizes memory usage.

## Why Does Python Reuse Some Objects?

Python reuses objects for immutable types (e.g., small integers, strings) to save memory and improve efficiency. However, for mutable objects (e.g., lists, dictionaries), Python creates a new object each time:

```python
list1 = [1, 2, 3]
list2 = [1, 2, 3]
print(id(list1), id(list2))  # Different IDs, as new objects are created.
```
## How Variables Work

-   Variables in Python are references to objects, not the objects themselves.
-   You can check the memory address of an object using id():
  
```python 
h = "hello world"
print(id(h))  # Prints the memory address of the object.
```

## Key Takeaways

-    **Everything in Python is an object**: From numbers to strings, everything has a type, value, and memory address.
-    **Variables point to objects**: Variables don’t hold values directly; they store references to objects in memory.
-    **Memory optimization**: Python reuses immutable objects like small integers and strings for efficiency.





