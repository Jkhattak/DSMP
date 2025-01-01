# Time Complexity
Time Complexity is a way to describe how the runtime of an algorithm changes as the size of the input grows.

When analyzing the time complexity of an algorithm we may find three cases:
- Best-case
- Average case
- Worst case

We are mathematical notation called **BIG-O** to describe time complexity.

## Big-O Notation 
Big-O notation, sometimes called `Asymptotic notation`, is a **mathmatical notation that describes the limiting behavior of a function** when the argument tends towards a particular value or infinity.

### Table of common time complexities 

| Name               | Time Complexity |
|--------------------|-----------------|
| Constant Time      | O(1)           |
| Logarithmic Time   | O(log n)       |
| Linear Time        | O(n)           |
| Quasilinear Time   | O(n log n)     |
| Quadratic Time     | O(n^2)         |
| Exponential Time   | O(2^n)         |
| Factorial Time     | O(n!)          |

![Big O Notation](bigONotation.png)

#### Order of Growth
- want to evaluate program's efficiency when **input is very big**
- Want to express the **growth of program's run time** as input size grows.
- Want to put an **upper bound** on growth-as tight as possible.
- do not need to be precise: **"order of"** not **exact** growth.
- we will look at the **largest factors** in runtime (which section of the program will take the longest to run).

```
def fact_iter(n):
    answer = 1 # 1 operation
    while n>1: # 1 operation
        answer *=n # 2 operation
        n-=1 # 2 operation
    return answer # 1 operation

```

***1 + 5n + 1*** is the equation of above code

#### Big 0 N steps


- ignore additive constants
- ignore multiplications constants


#### Law of Addition
- used with **sequential** statments

- ``` O(f(n) + O(g(n)) is O(f(n)) + g(n))```

for example:

```
for i in range(n):
  print('a')
  for j in range(n*n):
    print('b')

```
is ``` O(n) + O(n*n) = O(n+n^2) ``` because of domainant term

#### Law of multiplication
- used with nested loops
- ```O(f(n)) * O(g(n)) is O(f(n) * g(n))```
for example

```
for i in range(n):
    for j in range(n):
        print('a')
```

if `O(n)*O(n) = O(n*n) = O(n^2)` because the outer loops goes n times and the inner liip goes n times for every outer loop iter. 

```
number = int(input('Enter the number'))

digits = '0123456789'
result = ''

while number !=0:
    result = digits[number % 10] + result
    number = number//10

print(result)

```


***Big O of this would be log(n)***

---------

# Time Complexities

## Constant Time - O(1)
An algorithm is considered O(1) when its execution time does not depend on the size of the input. Regardless of how large or small the input is, the algorithm will always take the same amount of time to complete.

For example:

```python 
if a > b:
    print('True')
else:
    print('False')
```

## Logarithmic Time - O(log n)

Logarithmic time complexity refers to when the input data is divide into half
after iteration. 




