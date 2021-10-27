# Solution 4

## Exercise

Write a program according to the specification below.

### Specification

#### Input

* $$n$$ - natural number
* $$t1[n],\ t2[n]$$ - two lists of integers

#### Output

* The list created by adding a values from lists $$t1$$ and $$t2$$

## Solution

```python
n = int(input("Input number of elements: "))
tab1 = []
tab2 = []
result = []

for i in range(n):
  el = int(input("Input next element of the first list: "))
  tab1.append(el)

for i in range(n):
  el = int(input("Input next element of the second list: "))
  tab2.append(el)

for i in range(n):
    result.append(tab1[i] + tab2[i])

print("Result:", result)
```