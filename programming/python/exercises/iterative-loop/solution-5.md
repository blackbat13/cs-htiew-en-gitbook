# Solution 5

## Exercise

Write a program according to the specification below.

### Specification

#### Input

* $$n, k$$ - natural numbers, greater than zero
* $$n$$ natural numbers

#### Output

* Number of numbers divisible by $$k$$ from the given $$n$$ numbers

## Solution

```python
n = int(input("Input number of numbers: "))
k = int(input("Input divisor: "))

result = 0

for i in range(n):
    a = int(input("Input next number: "))
    if a % k == 0:
        result += 1

print(f"Number of numbers divisible by {k}: {result}")
```
