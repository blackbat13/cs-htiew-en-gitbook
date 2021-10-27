# Solution 4

## Exercise

Write a program according to the specification below.

### Specification

#### Input

* $$a, b$$ - two integers, greater than zero

#### Output

* The result of an integer division and the remainder of the division of numbers $$a$$ and $$b$$ 

## Solution

```python
a = int(input("Input first number: "))
b = int(input("Input second number: "))

division = a // b
remainder = a % b

print(a, "/", b, "=", division, ", remainder", remainder)
```