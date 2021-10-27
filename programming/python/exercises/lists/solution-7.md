# Solution 7

## Exercise

Write a program according to the specification below.

### Specification

#### Input

* $$n$$ - natural number
* $$tab[n]$$ - integers list

#### Output

* "Ascending" message if the list elements are sorted in ascending order
* "Descending" message if the list elements are sorted in descending order
* "Unsorted" message if the list elements are not sorted

## Solution

```python
n = int(input("Input number of elements: "))
tab = []

for i in range(n):
  el = int(input("Input next element: "))
  tab.append(el)

ascending = True
descending = True

for i in range(1, n):
    if tab[i] > tab[i - 1]:
        descending = False
    elif tab[i] < tab[i - 1]:
        ascending = False

if ascending:
    print("Ascending")
elif descending:
    print("Descending")
else:
    print("Unsorted")
```