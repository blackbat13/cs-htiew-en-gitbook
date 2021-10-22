# Solution 1

## Exercise

Write a program that complies with the specification below. Don't use **abs** function.

### Specification

#### Input

* $$a$$ - integer

#### Output

* The absolute value of $$a$$

## Solution

```python
a = int(input("Input a number: "))

if a < 0:
    a *= -1

print(f"Absolute value: {a}")
```