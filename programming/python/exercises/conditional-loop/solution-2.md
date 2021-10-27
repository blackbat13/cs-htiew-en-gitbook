# Solution 2

## Exercise

Write a program that complies with the specification below.

### Specification

#### Input

* $$n$$ - natural number

#### Output

* Sum of the digits of the number $$n$$

## Solution

```python
n = int(input("Input a number: "))

sum = 0

while n > 0:
    digit = n % 10
    sum += digit
    n = n // 10

print("Sum of digits:", sum)
```
