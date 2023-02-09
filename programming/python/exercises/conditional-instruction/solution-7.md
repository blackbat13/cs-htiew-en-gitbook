# Solution 7

## Exercise

Write a program according to the specification below.

### Specification

#### Input

* $$year$$ - natural number

#### Output

* A message stating whether the given year is a leap year or not

## Solution

```python
year = int(input("Input year: "))

if (year % 4 == 0 and year % 100 != 0) or year % 400 == 0:
    print(year, "is a leap year")
else:
    print(year, "is not a leap year")
```
