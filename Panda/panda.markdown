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
