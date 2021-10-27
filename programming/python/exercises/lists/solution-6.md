# Solution 6

## Exercise

Write a program according to the specification below.

### Specification

#### Input

* $$n$$ - natural number

#### Output

* $$mult[n][n]$$ - a two-dimensional array representing a multiplication table in the range $$[0,n-1]$$, where $$mult[i][j]=i*j$$

## Solution

```python
n = int(input("Input table size: "))
mult = []

for i in range(n):
    mult.append([])
    for j in range(n):
        mult[i].append(i * j)

print(mult)
```