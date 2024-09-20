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
