# Solution 6

## Exercise

Write a program according to the specification below.

### Specification

#### Input

* $$n$$ - natural number
* $$p$$ - natural number from the range $$[2,9]$$

#### Output

* The number $$n$$ represented in the system with the base $$p$$ 

## Solution

```python
n = int(input("Input a number: "))
system = int(input("Input the system: "))

new_number = ""

while n > 0:
    digit = n % system
    
    new_number = str(digit) + binary

    n = n // system

print("New representation:", new_number)
```
