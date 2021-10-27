# Solution 2

## Exercise

Write a program according to the specification below.

### Specification

#### Input

* $$n$$ - natural number
* $$a_1,a_2,\dots,a_n$$ - $$n$$ integers
* $$k$$ - natural number, $$1<=k<=n$$

#### Output

* $$a_k$$ - $$k$$-th given number

## Solution

```python
n = int(input("Input number of elements: "))
tab = []

for i in range(n):
  el = int(input("Input next element: "))
  tab.append(el)

k = int(input("Input element number: "))

print(tab[k - 1])
```