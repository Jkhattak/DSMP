# Numpy

NumPy (short for Numerical Python) is a library used for working with arrays and performing mathematical operations on large datasets efficiently. It is widely used in data science, machine learning, and scientific computing.

## Key Features

- Multidimensional Arrays:
    - NumPy provides the ndarray object, which supports multidimensional, homogeneous arrays (arrays of fixed data type).

- Mathematical Functions:
        Includes functions for statistical operations, linear algebra, Fourier transforms, and random number generation.

- Vectorized Operations:
    - Operations are applied element-wise to arrays without the need for explicit loops, making code faster and cleaner.

- Broadcasting:
    - Allows operations on arrays of different shapes and sizes seamlessly.

- Interoperability:
    - Easily integrates with other libraries like pandas, matplotlib, and scikit-learn.

## NumPy Arrays vs Python Sequences (Lists/Tuples)

Both NumPy arrays and Python sequences (like lists and tuples) are used to store collections of items, but they differ significantly in terms of functionality, performance, and efficiency. Here's a detailed comparison:

1. Data Type Consistency

    - NumPy Arrays:
        - Homogeneous: All elements must be of the same data type (e.g., all integers, all floats).
            Ensures memory efficiency and allows vectorized operations.
    - Python Sequences (Lists/Tuples):
        - Heterogeneous: Can store elements of different data types in the same sequence (e.g., integers, strings, floats).
        - Flexible but less efficient for numerical computations.

2. Performance
   - NumPy Arrays:
       - Optimized for numerical computations.
       - Operations on arrays are vectorized (performed at C-level speeds), making them much faster than Python loops.
   - Python Sequences:
       - Operations like summing or element-wise operations require explicit loops, which are slower in Python due to interpreter overhead.

3. Memory Efficiency

   - NumPy Arrays:
       - Use less memory because elements are stored in a contiguous block of memory.
       - Fixed data type for all elements results in reduced memory overhead.
   - Python Sequences:
       - Use more memory since each element is a Python object with additional metadata (like type, reference count).

| Feature                | NumPy Arrays               | Python Sequences (Lists/Tuples) |
|------------------------|----------------------------|----------------------------------|
| Data Type             | Homogeneous               | Heterogeneous                  |
| Speed                 | Faster                    | Slower                         |
| Memory Efficiency     | High                      | Low                            |
| Mathematical Operations| Built-in and Vectorized   | Manual Implementation Required |
| Multidimensional Data | Built-in Support          | Nested Lists                   |
| Flexibility           | Less Flexible             | More Flexible                  |

--- 

## Create Arrays

```python 
import numpy as np

arr = np.array([1, 2, 3, 4, 5])
print(arr)

# Output:
# [1 2 3 4 5]

```

## Array Initialization

`np.zeros()`

```python
zeros = np.zeros((2, 3))
print(zeros)

# Output:
# [[0. 0. 0.]
#  [0. 0. 0.]]
```

`np.ones()`

```python
ones = np.ones((3, 2))
print(ones)

# Output:
# [[1. 1.]
#  [1. 1.]
#  [1. 1.]]
```
`np.arange()` : Creates an array with evenly spaced values.

```python
arange = np.arange(1, 10, 2)
print(arange)

# Output:
# [1 3 5 7 9]
```

`np.reshape()` : Changes the shape of an array without changing its data.

```python
reshaped = np.arange(1, 10).reshape(3, 3)
print(reshaped)

# Output:
# [[1 2 3]
#  [4 5 6]
#  [7 8 9]]
```
`np.add()` : Adds two arrays element-wise.

```python
arr1 = np.array([1, 2, 3])
arr2 = np.array([4, 5, 6])
added = np.add(arr1, arr2)
print(added)

# Output:
# [5 7 9]
```
`np.multiply()` : Multiplies two arrays element-wise.

```python
multiplied = np.multiply(arr1, arr2)
print(multiplied)

# Output:
# [ 4 10 18]
```

`np.sqrt()` : Calculates the square root of each element

```python
sqrt = np.sqrt(np.array([1, 4, 9, 16]))
print(sqrt)

# Output:
# [1. 2. 3. 4.]
```
`np.linspace` : Linear spaced. It will create equal distant space numbers

```python 
# linear space
np.linspace(-10,10, 10, dtype=int)

# output
# array([-10,  -8,  -6,  -4,  -2,   1,   3,   5,   7,  10])
```

`np.identity()` : Creates a square identity matrix (diagonal elements are 1, rest are 0).

```python 
identity = np.identity(3)
print(identity)

# Output:
# [[1. 0. 0.]
#  [0. 1. 0.]
#  [0. 0. 1.]]
```

## Array Attribute

`np.ndim` : Returns the number of dimensions of an array.

```python 

arr = np.array([[1, 2, 3], [4, 5, 6]])
print(np.ndim(arr))

# Output:
# 2
```

`np.shape` : 
Returns the shape (dimensions) of an array as a tuple.

```python
arr = np.array([[1, 2, 3], [4, 5, 6]])
print(np.shape(arr))

# Output:
# (2, 3)
```

`np.size` : 
Returns the total number of elements in the array.

```python

import numpy as np

arr = np.array([[1, 2, 3], [4, 5, 6]])
print(np.size(arr))

# Output:
# 6
```

`np.itemsize` : 
Returns the size (in bytes) of each element in the array.

```Python
import numpy as np

arr = np.array([1, 2, 3], dtype=np.int32)
print(arr.itemsize)

# Output:
# 4  # Each integer occupies 4 bytes
```

`np.dtype` : 
Returns the data type of the elements in the array.

```python
import numpy as np

arr = np.array([1, 2, 3])
print(arr.dtype)

# Output:
# int64  # (on most systems; depends on platform)

```

## Changing Datatype

`np.astype` : 
Converts the data type of an array to the specified type.

```python
import numpy as np

arr = np.array([1.5, 2.7, 3.8])
converted = arr.astype(int)
print(converted)

# Output:
# [1 2 3]
```

## Array Operation 

- Arithmetic 
- Relational 
- Vector Operations

## Array Functions 
- max/min/sum/prod
- mean/median/std/var
- Dot product 
- log and exponents
- round/floor/ceil 

`np.mea(vector, axis=?)`

## Indexing and Slicing 

```python
c = np.arange(8).reshape(2,2,2)
a = np.arange(10)
b = np.arange(12).reshape(3,4)

print(b)

#output
array([[ 0,  1,  2,  3],
       [ 4,  5,  6,  7],
       [ 8,  9, 10, 11]])

b[1][2]

#output
6
```

```python 
b[1::,1::]

# output 
array([[ 5,  6,  7],
       [ 9, 10, 11]])
```

## Iteration 

```python 
for i in np.nditer(c):
    print(i)
```
## Stacking 

Two or more matrices can be stacked `horzantly` or `vertically`

- `np.vstack`
- `np.hstack`

## Numpy array vs Python List

NumPy is faster than Python lists because it uses C-style arrays, which store the actual values in a contiguous block of memory rather than storing references to memory addresses

- Time 
- Memory
- convenient 

```python 
#numpy array 
a = np.arange(10000000)
b = np.arange(10000000, 20000000)

start = time.time()
c = a + b 

print(time.time() - start)

#output 
0.1109921932220459
```

```python
# list 
import time 
a = [i for i in range(10000000)]
b = [i for i in range(10000000, 20000000)]
c = []

start = time.time()
for i in range(len(a)):
    c.append(a[i] + b[i])
print(time.time() - start)

#ouput
1.894963264465332

```

### Fancy indexing 

```python

a = array([[ 0,  1,  2],
       [ 3,  4,  5],
       [ 6,  7,  8],
       [ 9, 10, 11]])


a[[0,2,3]]

# ouput

array([[ 0,  1,  2],
       [ 6,  7,  8],
       [ 9, 10, 11]])
```

## Boolean Array in Python 

A boolean array is an array that contains True or False values. It is often used for boolean indexing, which helps filter data based on conditions.

```python 
import numpy as np

# Create a NumPy array
array = np.array([10, 20, 30, 40, 50])

# Boolean array: elements greater than 30
boolean_array = array > 30

# Use the boolean array to filter the data
filtered_array = array[boolean_array]

print(filtered_array)
# Output: [40 50]
```

## Broadcasting in Python

Broadcasting is a feature in Python (especially with NumPy) that allows arrays of different shapes to work together during arithmetic operations, without needing explicit loops or resizing.

When performing operations between arrays, broadcasting expands the smaller array's dimensions to match the larger one so the operation can proceed.

### Rules for Broadcasting

- The arrays must have compatible shapes:
    - If the dimensions are not the same, they are aligned starting from the rightmost dimension.
    - A dimension of size 1 in an array can be stretched to match the other array's size.

- If neither condition is met, broadcasting fails.

## Working with mathematical formulas 

### Sigmoid 
The sigmoid function is a mathematical function used widely in machine learning, especially in logistic regression and neural networks. It maps any real number into a range between 0 and 1, making it useful for probability-based models.

```python 
import numpy as np

# Define the sigmoid function
def sigmoid(x):
    return 1 / (1 + np.exp(-x))

# Example input
x = np.array([-5, 0, 5])

# Calculate sigmoid values
result = sigmoid(x)

print(result)
# Output: [0.00669285 0.5        0.99330715]
```

## Mean Squared Error (MSE)

The Mean Squared Error (MSE) is a common metric used to measure the average squared difference between the predicted values (y^y^​) and the actual values (yy). 
It evaluates how well a model's predictions match the actual data, with lower values indicating better performance.

```python 
import numpy as np

# Actual values
y = np.array([3, -0.5, 2, 7])

# Predicted values
y_pred = np.array([2.5, 0.0, 2, 8])

# Calculate MSE
mse = np.mean((y - y_pred) ** 2)

print("Mean Squared Error:", mse)
# Output: Mean Squared Error: 0.375
```

## Working with missing values 

```python 
a = np.array([1,2,3,4,np.nan,6])
a[~np.isnan(a)]
```

## Plotting graphs 

```python
import matplotlib.pyplot as plt
x = np.linspace(-10,10,100)
y = x

plt.plot(x,y)
```

![alt text](image.png)

## Numpy Tips and Tricks 

### Sort 
Will sort the numpy array 
```python
a = np.random.randint(1,100,20)

# ouput
array([ 2, 21, 28, 34, 39, 44, 48, 50, 50, 51, 54, 63, 65, 76, 80, 86, 93,
       95, 95, 99])
```

### Concatenate 
In NumPy, concatenation refers to combining two or more arrays along a specified axis. This is useful for merging datasets or reshaping data for further analysis.

```python 
numpy.concatenate((array1, array2, ...), axis=0)

```
#### Example 

```python 
import numpy as np

# Two 1D arrays
a = np.array([1, 2, 3])
b = np.array([4, 5, 6])

# Concatenate along the default axis (0)
result = np.concatenate((a, b))
print(result)
# Output: [1 2 3 4 5 6]

```

### Where
The np.where() function in NumPy is used to return elements from an array based on a condition. It works as a conditional operator, allowing you to choose values or indices where a condition is True.

```python
numpy.where(condition, [x, y])
```

```python 
import numpy as np

# Array
arr = np.array([10, 15, 20, 25, 30])

# Indices where elements are greater than 20
indices = np.where(arr > 20)
print(indices)
# Output: (array([3, 4]),)
```

```python
import numpy as np

# Array
arr = np.array([10, 15, 20, 25, 30])

# Replace values: if > 20, set to 1; else, set to 0
result = np.where(arr > 20, 1, 0)
print(result)
# Output: [0 0 0 1 1]
```

### Argmax
The np.argmax() function is used to find the index of the maximum value in a NumPy array. It is particularly useful in tasks like 
finding the most probable class in classification problems or identifying the largest value's position in an array.

```python
numpy.argmax(array, axis=None)
```

- `axis=None (default)` : Flattens the array and finds the maximum index globally.
- `axis=0` : Finds the maximum index along columns.
- `axis=1` : Finds the maximum index along rows.

### Append 

The np.append() function is used to add values to the end of an array. It creates a new array with the appended values, as NumPy arrays are immutable (cannot be modified in place).

```python
numpy.append(arr, values, axis=None)
```

### Cumsum

The np.cumsum() function computes the cumulative sum of elements along a specified axis. It returns an array where each element is the sum of all previous elements up to that position.
```python
numpy.cumsum(arr, axis=None)
```

### Percentile 

The np.percentile() function is used to compute the value below which a given percentage of data in an array falls. It is commonly used in statistics to determine thresholds like the median (50th percentile) or quartiles (25th and 75th percentiles).

```python
numpy.percentile(arr, q, axis=None, interpolation='linear', keepdims=False)
```
### Isin

The np.isin() function checks whether each element of an array exists in another array (or list) of values. It returns a boolean array of the same shape as the input array, indicating True for elements that are present in the specified values and False otherwise.

```python
numpy.isin(element, test_elements, assume_unique=False, invert=False)
```
#### Example 

```python
import numpy as np

# Input array
arr = np.array([1, 2, 3, 4, 5])

# Values to check against
values = [2, 4, 6]

# Check membership
result = np.isin(arr, values)
print(result)
# Output: [False  True False  True False]
```

### Put 
The np.put() function is used to modify specific elements in a NumPy array at given indices. It assigns new values to the specified positions in the array.

```python
import numpy as np

# Original array
arr = np.array([10, 20, 30, 40, 50])

# Replace elements at indices 1 and 3 with new values
np.put(arr, [1, 3], [99, 77])

print(arr)
# Output: [10 99 30 77 50]
```

