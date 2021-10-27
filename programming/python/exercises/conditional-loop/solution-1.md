# Solution 1

## Exercise

Write a program according to the specification below.

### Specification

#### Input

* $$n$$ - natural number

#### Output

* Successive digits of $$n$$, written from the end

## Solution

```python
n = int(input("Input a number: "))

while n > 0:
    digit = n % 10
    print(digit)
    n = n // 10
```