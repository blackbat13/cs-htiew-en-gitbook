# Solution 6

## Exercise

Write a program according to the specification below.

### Specification

#### Input

* $$n$$ - natural number

#### Output

* Multiplication table for the range $$[1,n]$$

## Solution

```python
n = int(input("Input table size: "))

for i in range(1, n + 1):
    for j in range(1, n + 1):
        print(i * j, end="")
    print()
```
