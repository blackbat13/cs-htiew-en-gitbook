# Solution 4

## Exercise

Write a program that complies with the specification below.

### Specification

#### Input

* $$n$$ - natural number
* $$k$$ - natural number from the range $$[0,9]$$

#### Output

* The number created by replacing each digit of the number $$n$$ by the absolute value of the difference between the number $$k$$ and the given digit

## Solution

```python
n = int(input("Input first number: "))
k = int(input("Input second number: "))

new_number = 0
power = 1

while n > 0:
    digit = n % 10
    
    diff = abs(k - digit)

    new_number += diff * power
    power *= 10

    n = n // 10

print("New number:", new_number)
```
