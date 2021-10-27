# Solution 1

## Exercise 

Write a program according to the specification below.

### Specification

#### Input

* $$n$$ - natural number

#### Output

* $$n!$$ - factorial of the number $$n$$

## Solution

```python    
n = int(input("Input number: "))
factorial = 1

for i in range(2, n + 1):
    factorial *= i

print(f"{n}! = {factorial}")
```
