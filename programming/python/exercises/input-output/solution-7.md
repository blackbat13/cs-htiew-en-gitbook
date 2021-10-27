# Solution 7

## Exercise 

Write a program according to the specification below.. Use the **max** function.

### Specification

#### Input

* $$a, b, c$$ - three integers

#### Output

* The largest of the numbers $$a$$, $$b$$ and $$c$$, or any when they are equal

## Solution

```python
a = int(input("Input first number: "))
b = int(input("Input second number: "))
c = int(input("Input third number: "))

result = max(a, b, c)

print("Max:", result)
```