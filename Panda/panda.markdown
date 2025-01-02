# Pandas

Pandas is a fast, flexible, and user-friendly open-source tool for data analysis and manipulation, built on Python.

## Pandas Series
A Pandas Series is like a column in a table. It is a 1-D array holding data of any type 

## Creating Series

```python

country = ['USA', 'India', 'Canada', 'China']

pd.Series(country)

# output
pd.Series(country)
```

####  Indexing and Naming Series

```python
country = ['USA', 'India', 'Canada', 'China']
championshsips = [90, 50, 60, 80]
championshsips = pd.Series(championshsips, index=country, name='Championships counts')

# output
USA       90
India     50
Canada    60
China     80
Name: Championships counts, dtype: int64
```

#### Dictioanry Series 

```python
medal = {
    'USA' :      990,
    'India' :    150,
    'Canada' :   160,
    'China' :    180,
}

pd.Series(medal, name='Medal Counts')

#output
USA       990
India     150
Canada    160
China     180
Name: Medal Counts, dtype: int64
```

## Size 

In pandas, .size is an attribute that returns the total number of elements in a Series or DataFrame. For a DataFrame, it is calculated as the product of rows and columns.

```python
import pandas as pd

# Create a DataFrame
data = {
    'Name': ['Alice', 'Bob', 'Charlie'],
    'Age': [25, 30, 35]
}
df = pd.DataFrame(data)

# Get the size of the DataFrame
print(df.size)  # Output: 6 (3 rows * 2 columns)

# Create a Series
series = pd.Series([10, 20, 30])

# Get the size of the Series
print(series.size)  # Output: 3
```

## Dtype
dtype in pandas refers to the data type of elements in a Series or the data types of each column in a DataFrame. It is short for "data type" and determines how the data is stored and processed.

```python
import pandas as pd

# Create a Series
series = pd.Series([1, 2, 3])
print(series.dtype)  # Output: int64

# Create a DataFrame
data = {
    'Name': ['Alice', 'Bob', 'Charlie'],
    'Age': [25, 30, 35],
    'Salary': [50000.0, 60000.5, 70000.8]
}
df = pd.DataFrame(data)

# Get the dtype of each column
print(df.dtypes)
# Output:
# Name       object
# Age         int64
# Salary    float64
```

## Is_unique

The is_unique attribute in pandas checks whether all the elements in a Series or the values in a DataFrame column are unique (i.e., no duplicates). It returns a boolean value: True if all values are unique, and False otherwise.

```python
import pandas as pd

# Create a Series with unique values
series1 = pd.Series([1, 2, 3, 4])
print(series1.is_unique)  # Output: True

# Create a Series with duplicate values
series2 = pd.Series([1, 2, 2, 4])
print(series2.is_unique)  # Output: False

# Create a DataFrame
data = {
    'ID': [101, 102, 103, 101],
    'Name': ['Alice', 'Bob', 'Charlie', 'Alice']
}
df = pd.DataFrame(data)

# Check uniqueness for a specific column
print(df['ID'].is_unique)  # Output: False
print(df['Name'].is_unique)  # Output: False
```

## Index

The index in pandas represents the labels or identifiers for the rows in a Series or DataFrame. It acts as a reference for accessing and aligning data. By default, pandas assigns a numerical index starting from 0, but it can be customized.

```python
import pandas as pd

# Create a DataFrame with default index
data = {'Name': ['Alice', 'Bob', 'Charlie'], 'Age': [25, 30, 35]}
df = pd.DataFrame(data)
print(df.index)
# Output: RangeIndex(start=0, stop=3, step=1)

# Create a DataFrame with a custom index
df_custom = pd.DataFrame(data, index=['A', 'B', 'C'])
print(df_custom.index)
# Output: Index(['A', 'B', 'C'], dtype='object')

# Access the index of a Series
series = pd.Series([10, 20, 30], index=['X', 'Y', 'Z'])
print(series.index)
# Output: Index(['X', 'Y', 'Z'], dtype='object')
```

## Values

The values attribute in pandas returns the underlying data of a Series or DataFrame as a NumPy array. It provides direct access to the data without the labels (index or column names).

```python
import pandas as pd

# Create a Series
series = pd.Series([1, 2, 3])
print(series.values)
# Output: [1 2 3] (NumPy array)

# Create a DataFrame
data = {
    'Name': ['Alice', 'Bob', 'Charlie'],
    'Age': [25, 30, 35]
}
df = pd.DataFrame(data)

print(df.values)
# Output:
# [['Alice' 25]
#  ['Bob' 30]
#  ['Charlie' 35]]
```

## Convert dataframe into series 

```python
import pandas as pd

# Read the CSV file and convert it to a Series
data = pd.read_csv('kohli_ipl.csv', index_col='match_no')
if len(data.columns) == 1:  # Check if there is only one column
    data = data.squeeze("columns")

print(data)
```

## Head 

Will show top(x) numbers of columns 

## Tail

Will show bottom(x) numbers of columns

## Value_Count

The `value_counts` method in panda is used to count the unique values in a Series. It returns a Series containing the counts of each unique_values, sorted in descending order by default. 

```python

Series.value_counts(normalize=False, sort=True, ascending=False, bins=None, dropna=True)
```

## Sort_Values 

The `sort_values` method in pandas is used to sort the values of a Series or Dataframe either in ascending or descending order 

```python
Series.sort_values(ascending=True, inplace=False, na_position='last')
```

## Inplace

The `inplace`  parameter in pandas is used to determine wheater a method modifies the original object directly or returns a modified copy 

- `inplace = True` : modifies the the original object directly without returning anything. 
- `inplace = False` : Returns a modified copy of the object, leaving the original unchanged

## Count

The `Count` method in Panda is used to count non-null (non-NaN) values in a Series or Dataframe. 

```python
Series.count()
```

## Math Operations
- Sum
- Product
- Mean
- Median
- Mode
- Std
- Var

## Indexing 

- Positional Indexing 
- Slicing 
- Fancy Indexing
- indexing with labels

## Editing Series
- Using indexing
- Slicing

## Series with Python Functionalities
- len
- type
- dir : All functions available on Series
- sorted
- max
- min

## Type Conversion 

 Type conversion in panda involves chanding the data type of a Series or Dataframe column to another type. This is often necessary to ensure data compatibility or optimize performance 

```python
import pandas as pd

# Create a DataFrame
data = {'A': ['1', '2', '3'], 'B': ['4.5', '5.5', '6.5']}
df = pd.DataFrame(data)

# Convert column 'A' to integers
df['A'] = df['A'].astype(int)

# Convert column 'B' to floats
df['B'] = df['B'].astype(float)

print(df)
# Output:
#    A    B
# 0  1  4.5
# 1  2  5.5
# 2  3  6.5
```

## Membership Operators
Membership operators are used to test wheater a value exists in a sequence (such as a list, tuple, string, or dictionary)

- Index based operator : `'Company (film)' in movies`
- Value based operator : `'Ajay Devgn' in movies.values`

## Arithmetic Operators 

```python
# Brocasting example
100 - runs_scored

#output
match1     0
match2    40
match3    30
match4    20
match5    10
match6     0
dtype: int64
```

## Astype 

The `astype()` method is used to cast a pandas Series or Dataframe
column to a specified data type. 

```python
DataFrame.astype(dtype, copy=True, errors='raise')
Series.astype(dtype, copy=True, errors='raise')
```
## Between 

The `between()` method in pandas is used to filter values in a Series that fall
between two specified boundries. It can include or exclude the boundry 
values based on the parameters. 

```python
Series.between(left, right, inclusive='both')
```

## Clip 
The `clip()` in pandas is used to clip values in a Series or Dataframe,
meaning values outside a specified range are replaced by the boundary
values (i.e., capped at a minimum or maximum)

```python 
Series.clip(lower=None, upper=None, axis=None, inplace=False)
DataFrame.clip(lower=None, upper=None, axis=None, inplace=False)
```

```python
import pandas as pd

# Create a Series
series = pd.Series([10, 20, 30, 40, 50])

# Clip values between 15 and 35
clipped_series = series.clip(lower=15, upper=35)
print(clipped_series)
# Output:
# 0    15
# 1    20
# 2    30
# 3    35
# 4    35
# dtype: int64
```
## Drop duplicates

The `drop_duplicates()` method in pandas removes duplicate rows from a DataFrame or duplicate elements from a Series.

```python
Series.drop_duplicates(keep='first', inplace=False)
```

```python 
import pandas as pd

# Create a DataFrame
data = {
    'Name': ['Alice', 'Bob', 'Alice', 'Charlie'],
    'Age': [25, 30, 25, 35]
}
df = pd.DataFrame(data)

# Remove duplicate rows
df_no_duplicates = df.drop_duplicates()
print(df_no_duplicates)
# Output:
#       Name  Age
# 0    Alice   25
# 1      Bob   30
# 3  Charlie   35
```

## Duplicated

The `duplicated()` method identifies duplicate rows or values in a Series or DataFrame and returns a boolean Series indicating whether each row/element is a duplicate.

```Python
Series.duplicated(keep='first')
```

```python 
import pandas as pd

# Create a DataFrame
data = {
    'Name': ['Alice', 'Bob', 'Alice', 'Charlie', 'Bob'],
    'Age': [25, 30, 25, 35, 30]
}
df = pd.DataFrame(data)

# Identify duplicate rows
print(df.duplicated())
# Output:
# 0    False
# 1    False
# 2     True
# 3    False
# 4     True
# dtype: bool
```

## Size 

The `size` attribute in pandas is used to return the total number of elements in a pandas object (Series or DataFrame). It is calculated as:

- For a `Series`: The total number of elements (equal to the length of the Series).
- For a `DataFrame`: The number of rows multiplied by the number of columns.

## Isnull
The `isnull()` method in pandas is used to detect missing values (NaN, None, or NaT) in a Series or DataFrame. It returns a boolean object of the same shape, where:

- `True` indicates a missing value.
- `False` indicates a non-missing value.

## Dropena
The `dropna()` method in pandas is used to remove missing values (NaN, None, or NaT) from a Series or DataFrame. It allows you to drop rows or columns containing missing values.

```python
import pandas as pd

# Create a DataFrame with missing values
data = {
    'A': [1, None, 3],
    'B': [4, 5, None],
    'C': [7, 8, 9]
}
df = pd.DataFrame(data)

# Drop rows with missing values
df_cleaned = df.dropna()
print(df_cleaned)
# Output:
#      A    B  C
# 0  1.0  4.0  7
```

## Fillna 
The `fillna()` method in pandas is used to replace missing values (NaN, None, or NaT) in a Series or DataFrame with a specified value or a strategy (e.g., forward fill, backward fill)

```python
import pandas as pd

# Create a DataFrame with missing values
data = {
    'A': [1, None, 3],
    'B': [4, 5, None],
    'C': [None, None, 9]
}
df = pd.DataFrame(data)

# Fill missing values with 0
df_filled = df.fillna(0)
print(df_filled)
# Output:
#      A    B    C
# 0  1.0  4.0  0.0
# 1  0.0  5.0  0.0
# 2  3.0  0.0  9.0
```

## Isin  
The `isin()` method in pandas is used to filter rows or elements in a Series or DataFrame by checking if they are present in a given list, set, or another iterable. It returns a boolean object of the same shape as the original, with True for values that are in the provided iterable and False otherwise.

```python
import pandas as pd

# Create a Series
series = pd.Series([1, 2, 3, 4, 5])

# Check if elements are in the list [2, 4, 6]
result = series.isin([2, 4, 6])
print(result)
# Output:
# 0    False
# 1     True
# 2    False
# 3     True
# 4    False
# dtype: bool

# Filter the Series
filtered = series[series.isin([2, 4, 6])]
print(filtered)
# Output:
# 1    2
# 3    4
# dtype: int64
```

## Apply 
The `apply()` method in pandas is used to apply a custom function or built-in function to each element of a pandas Series or to rows/columns of a DataFrame

```python 
DataFrame.apply(func, axis=0, raw=False, result_type=None, args=())
```
```python
import pandas as pd

# Create a Series
series = pd.Series([1, 2, 3, 4, 5])

# Apply a custom function to square each value
squared = series.apply(lambda x: x ** 2)
print(squared)
# Output:
# 0     1
# 1     4
# 2     9
# 3    16
# 4    25
# dtype: int64
```

## Copy 
The `copy()` method in pandas is used to create a copy of a pandas object (Series or DataFrame). This ensures that changes made to the copy do not affect the original object, and vice versa.

```python
import pandas as pd

# Create a DataFrame
data = {'A': [1, 2, 3], 'B': [4, 5, 6]}
df = pd.DataFrame(data)

# Create a deep copy
df_copy = df.copy()

# Modify the copy
df_copy['A'] = [10, 20, 30]

# Original DataFrame remains unchanged
print("Original DataFrame:")
print(df)
# Output:
#    A  B
# 0  1  4
# 1  2  5
# 2  3  6

print("\nModified Copy:")
print(df_copy)
# Output:
#     A  B
# 0  10  4
# 1  20  5
# 2  30  6
```

## View 
In pandas, a view refers to a subset of the original DataFrame or Series that reflects changes made to the original object, and vice versa. Unlike a copy, a view does not create a separate object in memory—it is a reference to the original data.

```python 
import pandas as pd

# Create a DataFrame
data = {'A': [1, 2, 3], 'B': [4, 5, 6]}
df = pd.DataFrame(data)

# Create a view (slicing)
view_df = df.loc[:, 'A']

# Modify the view
view_df.iloc[0] = 100

# Original DataFrame is updated
print("Original DataFrame after modifying the view:")
print(df)
# Output:
#      A  B
# 0  100  4
# 1    2  5
# 2    3  6
```

# Panda Dataframe

A DataFrame in pandas is a two-dimensional, tabular data structure with labeled rows and columns. You can create a DataFrame in several ways, depending on the source of your data.

```python
import pandas as pd

# Create a DataFrame from a dictionary
data = {
    'Name': ['Alice', 'Bob', 'Charlie'],
    'Age': [25, 30, 35],
    'Salary': [50000, 60000, 70000]
}
df = pd.DataFrame(data)
print(df)
# Output:
#       Name  Age  Salary
# 0    Alice   25   50000
# 1      Bob   30   60000
# 2  Charlie   35   70000
```
## Important functions to run on new dataset
- shape
- dtypes
- index
- columns
- values
- head/tail
- sample
- info
- describe
- isnull
- duplicated
- renames

## Rename
The rename() method in pandas is used to modify the labels of rows and/or columns in a DataFrame or Series. It allows for renaming specific labels or mapping them using a function.

```python
import pandas as pd

# Create a DataFrame
data = {'A': [1, 2, 3], 'B': [4, 5, 6]}
df = pd.DataFrame(data)

# Rename columns
renamed_df = df.rename(columns={'A': 'Column1', 'B': 'Column2'})
print(renamed_df)
# Output:
#    Column1  Column2
# 0        1        4
# 1        2        5
# 2        3        6
```

## Math Methods 

- Sum
- Min/Max
- Median
- Std

```python
students.sum(axis=1) #axis 1 allows summation on rows

#output
0    190
1    167
2    234
3    195
4      0
5      0
dtype: int64
```

## Selecting rows from a Dataframe

- iloc - searches using index Position
- loc - searches using index labels 

### loc: Label-Based Indexing

-    loc selects data based on row and column labels.
-    You use the names of rows and columns to extract data.
-    Can include boolean arrays or conditions.
-    Includes both the start and end index when slicing.


```python
import pandas as pd
df = pd.DataFrame({'A': [1, 2, 3], 'B': [4, 5, 6]}, index=['x', 'y', 'z'])

# Using loc with row labels
print(df.loc['x'])  # Row labeled 'x'
# Output: A    1
#         B    4

# Using loc with both row and column labels
print(df.loc['x', 'A'])  # Value at row 'x' and column 'A'
# Output: 1

# Slicing with loc
print(df.loc['x':'y'])  # Rows from 'x' to 'y' (inclusive)
# Output: A  B
#         x  1  4
#         y  2  5

```
### iloc

iloc: Position-Based Indexing

-    iloc selects data based on row and column positions (numerical index).
-    You use numbers to specify row and column locations.
-    Excludes the end index when slicing.   
```python
# Using iloc with row positions
print(df.iloc[0])  # First row (position 0)
# Output: A    1
#         B    4

# Using iloc with both row and column positions
print(df.iloc[0, 0])  # Value at 1st row, 1st column
# Output: 1

# Slicing with iloc
print(df.iloc[0:2])  # Rows from position 0 to 1 (2 is excluded)
# Output: A  B
#         x  1  4
#         y  2  5
```