# Solution 5

## Exercise

Write a program that complies with the specification below.

### Specification

#### Input

* $$n$$ - natural number

#### Output

* Binary representation of the number $$n$$

## Rozwiązanie

```python
n = int(input("Input a number: "))

binary = ""

while n > 0:
    digit = n % 2
    
    binary = str(digit) + binary

    n = n // 2

print("Binary representation:", binary)
```