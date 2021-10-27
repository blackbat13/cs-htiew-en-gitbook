# Solution 6

## Exercise

Write a program according to the specification below. Use the **min** function.

### Specification

#### Input

* $$a, b$$ - two integers

#### Output

* The smaller of the numbers $$a$$ and $$b$$, or any number, when they are equal to each other

## Solution

```python
a = int(input("Input first number: "))
b = int(input("Input second number: "))

result = min(a, b)

print("Min:", result)
```