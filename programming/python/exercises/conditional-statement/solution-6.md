# Solution 6

## Exercise

Write a program according to the specification below. Take care of the program readability.

### Specification

#### Input

* $$a, b$$ - two integers
* $$op$$ - sign of one of the allowed operations: $$+,-,*,/$$ 

#### Output

* Result of an operation $$a\ op\ b$$ (e.g. $$a+b$$), or a message that division could not be performed.

## Solution

```python
a = int(input("Input first number: "))
b = int(input("Input second number: "))
op = input("Input operation symbol: ")

if op == "+":
    print(a, "+", b, "=", a + b)
elif op == "-":
    print(a, "-", b, "=", a - b)
elif op == "*":
    print(a, "*", b, "=", a * b)
else:
    if b == 0:
        print("Cannot divide by 0!")
    else:
        print(a, "/", b, "=", a / b)
```