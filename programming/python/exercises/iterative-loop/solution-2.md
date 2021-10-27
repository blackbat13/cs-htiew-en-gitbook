# Solution 2

## Exercise

Write a program according to the specification below. Do not use the `**` operator.

### Specification

#### Input

* $$a, n$$ - two natural numbers

#### Output

* $$a^n$$ 

## Solution

```python
a = int(input("Input first number: "))
n = int(input("Input second number: "))

result = 1

for i in range(1, n + 1):
    result *= a

print(f"{a}^{n} = {result})
```
