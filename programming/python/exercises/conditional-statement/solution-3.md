# Solution 3

## Exercise

Write a program according to the specification below.

### Specification

#### Input

* $$a, b$$ - two integers

#### Output

* The result of dividing numbers $$a$$ and $$b$$, or a message that division could not be performed.

## Solution

```python
a = int(input("Input first number: "))
b = int(input("Input second number: "))

if b == 0:
    print("Cannot divide by 0!")
else:
    result = a / b
    print(a, "/", b, "=", result)
```