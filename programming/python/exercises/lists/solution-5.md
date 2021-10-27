# Solution 6

## Exercise

Write a program according to the specification below.

### Specification

#### Input

* $$n$$ - natural number

#### Output

* $$fib[n]$$ - list containing $$n$$ consecutive Fibonacci numbers

## Solution

```python
n = int(input("Input number: "))
fib = [1, 1]

for i in range(2, n):
  fib[i] = fib[i - 2] + fib[i - 1]

print("Fibonacci numbers:", fib)
```