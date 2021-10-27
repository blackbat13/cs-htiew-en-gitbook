# Solution 8

## Exercise

Write a program according to the specification below.

### Specification

#### Input

* $$n$$ - natural number

#### Output

* All triples of natural numbers whose sum is equal to $$n$$

## Solution

```python
n = int(input("Input number: "))

for i in range((n // 3) + 1):
    for j in range(i, ((n - i) // 2) + 1):
        print(f"({i}, {j}, {n - i - j})")
```
