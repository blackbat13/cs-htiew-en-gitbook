# Solution 3

## Exercise

Write a program according to the specification below.

### Specification

#### Input

* $$n$$ - natural number
* $$a_1,a_2,\dots,a_n$$ - $$n$$ integers
* $$p, k$$ - two natural numbers, $$1<=p,k<=n$$, $$p <= k$$

#### Output

* $$a_p+a_{p+1}+a_{p+2}+...+a_{k}$$ - sum of values at positions from $$p$$ to $$k$$

## Solution

```python
n = int(input("Input number of elements: "))
tab = []

for i in range(n):
  el = int(input("Input next element: "))
  tab.append(el)

p = int(input("Input first position: "))
k = int(input("Input last position: "))

result = 0

for i in range(p, k + 1):
    result += tab[i]

print("Sum:", result)
```