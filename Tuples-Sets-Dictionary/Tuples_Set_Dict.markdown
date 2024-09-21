# Tuples - Sets - Dictionary
---

## Tuple

A *tuple& in Python is similar to a list. The difference between the two is that we cannot change the elements of a tuple once it is assigned, whereas we can change the elements of a list.

In short, a tuple is an immutable list. A tuple cannot be changed in any way once it is created.

### Characteristics

- Ordered
- Unchangeable
- Allows duplicates

Single item tuple **must have a comma** after the item

```
t = (1)
print(type(t))

--output--
<class 'int'>
```
```
# Single item tuple
t = (1,)
print(t)

--output--
(1,)

```
```
# Tuple within a tuple
t = (1,2,3,4,(5,6))

print(type(t))

--output--
<class 'tuple'>
```

### Accessing item within tuple

- Indexing
- Slicing 

```
t = (1,2,3,4,(5,6))
print(t[3])

--output
4
```
```
t = (1,2,3,4,(5,6))
print(t[0:3])

--output--
(1, 2, 3)
```

```
t = (1,2,3,4,(5,6))
print(t[-1][1])

--output--
6
```
## Editing in tuples 

Tuples can not be modified once created

```
t = (1,2,3,4,5)
t[0] = 100

--output--
TypeError                                 Traceback (most recent call last)
Cell In[12], line 2
      1 t = (1,2,3,4,5)
----> 2 t[0] = 100

TypeError: 'tuple' object does not support item assignment
```

### Del keyword

The whole tuple can be deleted; however, a single item in tuple cannot be deleted. 

```
t = (1,2,3,4,5)
del(t[0])

--output--

TypeError                                 Traceback (most recent call last)
Cell In[14], line 2
      1 t = (1,2,3,4,5)
----> 2 del(t[0])

TypeError: 'tuple' object doesn't support item deletion
```
## Operations on Tuple

- Addition
- Multiplication
- Membership
- Iteration

```
t = (1,2,3,4,5)
t2 = (6,7,8,9,10)

print(t+t2)

--output--
(1, 2, 3, 4, 5, 6, 7, 8, 9, 10)
```
```
#membership
t = (1,2,3,4,5)

1 in t
```
```
#iteration
t = (1,2,3,4,5)

for i in t:
    print(i)
```

## Tuple functions
- len
- min
- max
- sorted
- sum
- Count
- Index
```
t = (1,2,3,4,5)

sorted(t)

--output--
[1, 2, 3, 4, 5]
```
```
#index
t = (1, 2, 3, 4, 5)

t.index(5)

--output--
4

```
### Main difference between lists and tuples
- Syntax
- Mutability
- Speed (`Tuples` are `faster` than `list`)
- Memory (`Tuples` takes `less memory` compared to `list`)
- Built in functionality
- Error Prone
- Usability
```
# Error prone
a = [1,2,3]
b = a
a.append(4)
print(a)
print(b)

--output--
[1, 2, 3, 4]
[1, 2, 3, 4]
```
```
a = (1,2,3)
b = a
a = a + (4,)
print(a)
print(b)

--output--
(1, 2, 3, 4)
(1, 2, 3)
```

### Tuple unpacking
```
a,b,c=(1,2,3)
print(a,b,c)

--output--
1 2 3
```
```
#Swaping variables
a = 1
b=2
a,b = b,a
print('a',a)
print('b', b)

--output
a 2
b 1
```
```
a,b,*other=(1,2,3,4,5)

print('a is', a,',b is', b,',and others are',other)

--output--
a is 1 ,b is 2 ,and others are [3, 4, 5]
```

### Zipping tuples
```
a = (1,2,3,4)
b = (5,6,7,8)

list(zip(a,b))

--output--
[(1, 5), (2, 6), (3, 7), (4, 8)]
```
## Sets
A set is an unordered collection of items. Every set element is unique (no duplicates) and must be immutable (cannot be changed); However, a set itself is mutable. We can add or remove items from it. 

Set can also be used to perform mathematical set operations like union, intersection, symmetric difference, etc

### Characteristics:
 - Unordered
 - Mutable
 - No Duplicates
 - Can't contain mutable data types

```
empty_set = set()
print(empty_set)

--output--
set()
```
```
#2d set
s2 = {1,2,3,{1,2}}
print(s2)

--output--
TypeError                                 Traceback (most recent call last)
Cell In[28], line 2
      1 #2D set
----> 2 s2 = {1,2,3,{1,2}}
      3 print(s2)

TypeError: unhashable type: 'set'
```
```
t = {1,2,3,'hello', True, (1,2,3,'hello')}
print(t)

--output--
{1, 2, 3, (1, 2, 3, 'hello'), 'hello'}
```
- `1` and `True` are treated same by python

**Extracting item via `indexing or slicing` can not be performed since it does not have an order**

### Adding item in list
```
# Adding item 
s = {1,2,3,4,5}
s.add(5)
print(s)

--output--
{1, 2, 3, 4, 5}
```
```
# Updating : Can add multiple items at once

s.update([6,7,7])
print(s)

--output--
{1, 2, 3, 4, 5, 6, 7}
```
### del
Can be used to delete whole set instead of single item

```
del s[0]

--output--
Cell In[34], line 1
----> 1 del s[0]

TypeError: 'set' object doesn't support item deletion
```
