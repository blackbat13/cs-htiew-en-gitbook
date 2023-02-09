# Solution 4

## Exercise 4

Write a program according to the specification below. Don't use **min** and **max** functions.

### Specification

#### Input

* $$a, b, c$$ - three integers

#### Output

* The largest of the numbers $$a$$, $$b$$ and $$c$$, or any when they are equal.

## Solution

```python
a = int(input("Input first number: "))
b = int(input("Input second number: "))
c = int(input("Input third number: "))

if a >= b and a >= c:
    print("Max:", a)
elif b >= a and b >= c:
    print("Max:", b)
else:
    print("Max:", c)
```

