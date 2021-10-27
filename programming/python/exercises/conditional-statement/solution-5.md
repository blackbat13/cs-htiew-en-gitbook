# Solution 5

## Exercise

Write a program according to the specification below. Don't use **min** and **max** functions.

### Specification

#### Input

* $$a, b, c, d$$ - four integers

#### Output

* The largest of the numbers $$a, b, c$$ and $$d$$, or any when they are equal.

## Solution

```python
a = int(input("Input first number: "))
b = int(input("Input second number: "))
c = int(input("Input third number: "))
d = int(input("Input fourth number: "))

if a >= b and a >= c and a >= d:
    print("Max:", a)
elif b >= a and b >= c and b >= d:
    print("Max:", b)
elif c >= a and c >= b and c >= d:
    print("Max:", c)
else:
    print("Max:", d)
```