# Solution 8

Write a program according to the specification below.

### Specification

#### Input

* $$n$$ - natural number
* $$p, k$$ - two natural numbers, $$p <= k$$

#### Output

* $$n$$-elements list filled with random values from the range $$[p, k]$$

## Solution

```python
import random


n = int(input("Number of elements: "))
p = int(input("Range beginning: "))
k = int(input("Range end: "))

tab = [random.randint(p, k) for _ in range(n)]

print(tab)
```