# Tips and Tricks

## Introspection 

Using a `question mark (?)` before or after a variable will display some general information about the object

```python 
def add(a,b):
    return a + b

?add # 

--output--

Signature: add(a, b)
Docstring: <no docstring>
File:     file.py
Type:      function
```
## Everything is an object
Every **number, string, data structure, function, class, module, and so on** exists in python
interpretor in its own `box` which is referred to as a python object. 

## Variable and argument passing

### Object Creation:

-    In Python, when you write `x = 1`, Python creates an object representing the `integer 1`, which includes both the `value (1)`
`and metadata (e.g., type information that says it's an integer)`. This is different from lower-level languages like C++ and Java,
where the type is explicitly declared and memory is allocated directly for the variable.

### Reference Assignment (Name Binding):

-    Python then creates a `reference (or "name binding") from the variable x to the integer object 1`. 
`Here, x doesn’t contain 1 itself; instead, it holds a reference (or address) to the object that represents 1.`
-    In contrast, languages like C++ and Java handle variables differently. In Java, for example, 
primitive types are stored directly in the variable, while for objects, variables contain references to memory locations (similar to Python but only for non-primitive types).

### Dynamic Typing:

-    Python allows this dynamic association where x can later point to a different type of object, say x = "hello", without 
changing its `type.` The type is associated with the object, not the variable x. This differs from statically typed languages like 
C++ and Java, where the `type of x is fixed once declared.`

### Garbage Collection:

-    When x is reassigned to a new object, Python’s garbage collector can clean up the original object if there are no remaining references to it, which is an automatic process that’s different from manual memory management in languages like C++.

## Isinstance 

Isinstance function can be used to check wheather a variable has specific data type.

## Binary Operators 

### Table 2-3. Binary Operators

| Operation | Description |
|-----------|-------------|
| `a + b`   | Add `a` and `b` |
| `a - b`   | Subtract `b` from `a` |
| `a * b`   | Multiply `a` by `b` |
| `a / b`   | Divide `a` by `b` |
| `a // b`  | Floor-divide `a` by `b`, dropping any fractional remainder |
| `a ** b`  | Raise `a` to the `b` power |
| `a & b`   | `True` if both `a` and `b` are `True`; for integers, take the bitwise AND |
| `a \| b`   | `True` if either `a` or `b` is `True`; for integers, take the bitwise OR |
| `a ^ b`   | For booleans, `True` if `a` or `b` is `True`, but not both; for integers, take the bitwise EXCLUSIVE-OR |
| `a == b`   | `True` if `a` equals `b` |
| `a != b`   | `True` if `a` is not equal to `b` |
| `a <= b`, `a < b` | `True` if `a` is less than (less than or equal to) `b` |
| `a >= b`, `a > b` | `True` if `a` is greater than (greater than or equal to) `b` |
| `a is b`   | `True` if `a` and `b` reference the same Python object |
| `a is not b` | `True` if `a` and `b` reference different Python objects |
