# Solution 4

## Exercise

Write a program according to the specification below.

### Specification

#### Input

* $$n$$ - natural number, greater than $$0$$ 
* $$n$$ natural numbers

#### Output

* Maximum of the given $$n$$ numbers

## Solution

```python
n = int(input("Input number of numbers: "))

result = 0

for i in range(n):
    a = int(input("Input next number: "))
    if a > result:
        result = a

print("Max:", result)
```
