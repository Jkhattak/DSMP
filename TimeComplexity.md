# Time Complexity
Time Complexity is a way to describe how the runtime of an algorithm changes as the size of the input grows.

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

![Big O Notation](8psl4kk-1450149829.png)


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


```
