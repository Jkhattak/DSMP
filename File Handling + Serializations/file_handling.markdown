# File Handling + Serialization & Deserialization 


### What is File Handling?
File handling in Python allows you to interact with files to perform operations such as reading from and writing to files. Python provides built-in functions and methods to handle files, making it easy to work with both text and binary data.

---

### Types of Data Used for I/O
File handling can be categorized into two main types based on the data format:

1. **Text Files**
2. **Binary Files**

---

### 1. Text Files
- **Definition**: Text files store data in a human-readable format, such as plain text. Each line of text ends with a special character known as the **newline character** (`\n`).
- **Common Examples**: `.txt`, `.csv`, `.html`, `.py`, etc.
- **Encoding**: Text files are usually encoded in formats like `UTF-8` or `ASCII`.

#### Operations on Text Files
- **Reading**: Using methods like `read()`, `readline()`, and `readlines()`.
- **Writing**: Using methods like `write()` and `writelines()`.

#### Example
```python
# Writing to a text file
with open("example.txt", "w") as file:
    file.write("Hello, World!\n")
    file.write("This is a text file.")

# Reading from a text file
with open("example.txt", "r") as file:
    content = file.read()
    print(content)
```
---

### 2. Binary Files

- Definition: Binary files store data in a binary (non-human-readable) format, which includes images, videos, audio files, and executable files. The data is stored as a sequence of bytes.
    - Common Examples: .jpg, .png, .mp3, .bin, .exe, etc.

#### Operations on Binary Files

- Reading: Using rb mode to read in binary format.
- Writing: Using wb mode to write in binary format.

```python
# Writing to a binary file
data = bytes([120, 3, 255, 0, 100])  # A sample byte sequence
with open("example.bin", "wb") as file:
    file.write(data)

# Reading from a binary file
with open("example.bin", "rb") as file:
    binary_content = file.read()
    print(binary_content)
```
---

## File Modes in Python

Python provides various modes to open a file:

- **"r"**: Read mode (default). Opens a file for reading.
- **"w"**: Write mode. Opens a file for writing (overwrites the file if it exists).
- **"a"**: Append mode. Opens a file for appending (adds data to the end of the file).
- **"b"**: Binary mode. Used with `r`, `w`, or `a` to work with binary files.
- **"x"**: Exclusive creation. Creates a file, but raises an error if the file already exists.
- **"t"**: Text mode (default). Used with `r`, `w`, or `a` for text files.

---

### Combined Modes

- **"rb"**: Read binary
- **"wb"**: Write binary
- **"rt"**: Read text (default)
- **"wt"**: Write text (default)

## Summary

- `Text Files:` Human-readable format, commonly used for plain text and structured data like CSV.
- `Binary Files:` Non-human-readable format, used for images, videos, and other binary data.
- `File Modes:` Determine how a file is opened and what operations are allowed.

## How the `open()` Function Works at the Memory Level

The `open()` function in Python is a high-level interface for interacting with the underlying operating system's file system. Understanding how it works at the memory level gives insight into how files are accessed and manipulated efficiently.

---

### 1. **High-Level Overview**
When you call `open()`, Python interacts with the operating system (OS) to access the file system. The OS is responsible for managing files and memory resources. Here's what happens in detail:

1. **System Call**: The `open()` function makes a system call to the OS to request access to a specific file. A system call is a way for a program to communicate with the kernel of the operating system.
2. **File Descriptor**: If the file is successfully opened, the OS assigns a unique **file descriptor**. This is a low-level integer handle that represents the open file. The file descriptor acts as an index into a table maintained by the OS that keeps track of all open files.
3. **Buffering**: The `open()` function may also create a **buffer** in memory, depending on the mode specified (e.g., text or binary mode). Buffering helps optimize file I/O by reducing the number of direct disk access operations.
4. **File Object**: At a higher level, Python wraps this file descriptor in a **file object**, providing a more user-friendly way to interact with the file (e.g., reading or writing data).

---

### 2. **Memory Allocation and Buffers**
- **Text Mode (`"t")**: When a file is opened in text mode, Python uses a **text buffer**. The data is read or written as characters and automatically converted to or from a specific encoding (like UTF-8). This text buffer is allocated in memory to hold a chunk of the file content temporarily.
- **Binary Mode (`"b")**: In binary mode, a **binary buffer** is used, and data is read or written as raw bytes. No encoding conversion occurs in this mode.

#### Buffer Types
- **Full Buffering**: Data is buffered until the buffer is full before writing to the file or reading from it.
- **Line Buffering**: Data is buffered until a newline character is encountered.
- **Unbuffered**: No buffering occurs, and every read or write operation is immediately reflected in the file.

---

### 3. **Reading and Writing Data**
- **Reading**: When you use methods like `read()` or `readline()`, the data is read from the buffer into memory. If the buffer is empty, the OS reads a chunk of data from the file on disk and loads it into the buffer.
- **Writing**: When you write data using `write()`, it is first placed into the buffer. The data is only written to disk when the buffer is flushed (either manually or automatically when the buffer is full or the file is closed).

---

### 4. **Memory Management**
- **Garbage Collection**: Python uses automatic garbage collection to manage memory. When a file object is no longer in use (e.g., it goes out of scope or is explicitly closed), Python deallocates the memory used by the buffer and the file object.
- **Closing the File**: Always use `close()` or a `with` statement to ensure the file is properly closed, releasing the file descriptor and flushing any remaining data in the buffer.

---

### 5. **Summary of Memory-Level Operations**
1. `open()` makes a system call to the OS.
2. The OS assigns a file descriptor and may allocate buffers in memory.
3. Python creates a file object, which provides a high-level interface for file operations.
4. Data is read from or written to the buffer before being reflected in the file on disk.

### Example
```python
# Using `with` ensures proper closing of the file and memory cleanup
with open("example.txt", "r") as file:
    content = file.read()
    # `content` is loaded into memory from the buffer
```
---

## Using a Context Manager with `open()`

### What is a Context Manager?
A **context manager** in Python is a construct that allows you to allocate and release resources precisely when you want. The `with` statement is used to simplify working with context managers and ensures that resources, like file handles, are properly released when they are no longer needed.

---

### Why Use a Context Manager with `open()`?
When you open a file using `open()`, it’s essential to close the file after you’re done to free up system resources. If you forget to close the file, it can lead to memory leaks or locked files. The `with` statement ensures that the file is automatically closed, even if an error occurs.

---

### Syntax
```python
with open("filename", "mode") as file:
    # Perform file operations
```

### Tell and Seek Function 

- `seek(offset, whence):` Moves the file pointer to a specified byte position. The offset indicates how many bytes to move, and whence defines the reference point (start, current position, or end of file). Default is 0 (start of the file).

- `tell():` Returns the current byte position of the file pointer within the file. This is useful for checking where the pointer is located after using seek() or reading data.

```python
with open("example.txt", "rb") as file:
    file.seek(5)              # Move pointer to byte 5
    print(file.tell())        # Output current position (should be 5)
    
    data = file.read(10)      # Read next 10 bytes from position 5
    print(data)               # Print the data read
    print(file.tell())        # Output new position after read
```

### Problems with working in text mode

- Can't work with binary files like `images`
- Not good for other data types like int/float/list/tuples

## Working with Binary Files

```python
with open('Capture.PNG', 'rb') as f: #READ BINARY
    with open('screenshot_copy.jpg', 'wb') as wf: #WRITE BINARY
        wf.write(f.read()) #WRITE BACK TO COPY
```

### Working with Other Data Types

- `Text` files can only have `string` data type. 
- `Must` convert string to `differe data types` to work with `non-string` data type. 


## Serialization and Deserialization 

`Serialization` and `Deserialization` are processes used to convert data structures or objects into a format that can be stored or transmitted, and then reconstruct them back into the original structure or object.

### Serialization

Serialization is the process of converting a Python object (such as a list, dictionary, or custom class instance) into a format that can be easily stored or transmitted. Common formats include binary, JSON, or XML.

- **Purpose**: To save the object state to a file, database, or to send it over a network.
- **Common Modules**: pickle (for binary serialization), json (for JSON serialization).

### Deserialization

`Deserialization` is the reverse process, where the serialized data is read from a file or other storage medium and reconstructed back into a Python object.

- **Purpose**: To retrieve the original object from the stored format.
- **Common Modules**: pickle (binary deserialization), json (JSON deserialization).

`JSON`: Javascript on notation


```python
import json

data = {"name": "Alice", "age": 30}

# Serialization to JSON format
with open("data.json", "w") as file:
    json.dump(data, file)

# Deserialization from JSON format
with open("data.json", "r") as file:
    loaded_data = json.load(file)
    print(loaded_data)  # Output: {'name': 'Alice', 'age': 30}
```

### Serialization & Deserialization of Tuples

When it comes it `**tuples**`, the json will **`always`** write it as a list and retrieve it as a list

## Pickling 

**`Picking`** is the process whereby a python object hierarchy is converted into a byte stream, and **`unpickling`** is the inverse operation, whereby a byte stream (from a binary file or bytes-like object) is converted back into an object hierarchy. 

```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

# Create an instance of Person
person = Person("Alice", 30)

# Pickling the custom object
with open("person.pkl", "wb") as file:
    pickle.dump(person, file)

# Unpickling the custom object
with open("person.pkl", "rb") as file:
    loaded_person = pickle.load(file)
    print(loaded_person.name, loaded_person.age)  # Output: Alice 30
```

**`Pickle`**: Best for Python-specific, complex objects but unsafe for untrusted sources.
**`JSON`**: Ideal for simple, cross-platform data sharing and is safer to use.




