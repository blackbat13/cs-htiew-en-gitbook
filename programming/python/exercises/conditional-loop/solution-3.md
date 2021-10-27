# Solution 3

## Exercise

Write a program according to the specification below.

### Specification

#### Input

* $$n$$ - natural number

#### Output

* The number created by reversing the digits of the number $$n$$

## Solution

```python
n = int(input("Input a number: "))

reversed = 0

while n > 0:
    digit = n % 10
    
    reversed *= 10
    reversed += digit

    n = n // 10

print("Reversed number:", reversed)
```
