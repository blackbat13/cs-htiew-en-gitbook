# Solution 7

## Exercise

Write a program according to the specification below.

### Specification

#### Input

* $$n$$ - natural number

#### Output

* All pairs of natural numbers whose sum is equal to $$n$$

## Solution

```python
n = int(input("Input number: "))

for i in range((n // 2) + 1):
    print(f"({i}, {n - i})")
```
