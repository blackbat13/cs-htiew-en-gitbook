# Solution 2

## Exercise 

Write a program according to the specification below.

### Specification

#### Input

* $$a$$ - integer

#### Output

* The sign of the number $$a$$, i.e. $$1$$ when $$a$$ is positive, $$-1$$ when $$a$$ is negative, $$0$$ when $$a$$ is equal to $$0$$ 

## Solution

```python
a = int(input("Input number: "))

if a < 0:
    print("The sign of given number is -1")
elif a > 0:
    print("The sign of given number is 1")
else:
    print("The sign of given number is 0")
```