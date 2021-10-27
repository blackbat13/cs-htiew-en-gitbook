# Solution 1

# Exercise

Write a program according to the specification below.

### Specification

#### Input

* $$n$$ - natural number
* $$a_1,a_2,\dots,a_n$$ - $$n$$ integers

#### Output

* $$a_n,a_{n-1},\dots,a_2,a_1$$ - given numbers in reverse order

## Solution

```python
n = int(input("Input number of elements: "))
tab = []

for i in range(n):
  el = int(input("Input next element: "))
  tab.append(el)

for i in range(n - 1, -1, -1):
  print(tab[i])
```