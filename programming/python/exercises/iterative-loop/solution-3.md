# Solution 3

## Exercise

Write a program according to the specification below.

### Specification

#### Input

* $$n$$ - natural number
* $$n$$ integers

#### Output

* Sum of the given $$n$$ integers

## Solution

```python
n = int(input("Input number of numbers: "))

result = 0

for i in range(n):
    a = int(input("Input next number: "))
    result += a

print("Sum:", result)
```
