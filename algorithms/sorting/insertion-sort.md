---
description: Insertion sort
---

# Insertion sort

## Problem description

<!-- TODO -->

### Specification

#### Input:

* $$n$$ - natural number, number of elements in the array
* $$A[1..n]$$ - array of $$n$$ integers

#### Output:

* Array $$A$$ sorted in ascending order 

### Example

#### Input

```
n := 8
A := [6, 5, 3, 1, 8, 7, 2, 4]
```

#### Animation 1

![By Swfung8 - Own work, CC BY-SA 3.0, https://commons.wikimedia.org/w/index.php?curid=14961606](../../.gitbook/assets/Insertion-sort-example-300px.gif)

#### Animation 2

{% embed url="https://blackbat13.github.io/visul2/sorting/insertion_sort/#array=%5B6%2C5%2C3%2C1%2C8%2C7%2C2%2C4%5D" %}

## Solution

<!-- TODO -->

### Pseudocode

```
procedure Insertion(A, n):
    1. For i := 2 to n, do:
        2. j := i
        3. While j > 1 and A[j] < A[j-1], then:
            4. Swap(A[j], A[j - 1])
```

### Complexity

$$O(n^2)$$ - square

## Implementation

### C++

{% content-ref url="../../programming/c++/algorithms/sorting/insertion-sort.md" %}
[insertion-sort.md](../../programming/c++/algorithms/sorting/insertion-sort.md)
{% endcontent-ref %}

### Python

{% content-ref url="../../programming/python/algorithms/sorting/insertion-sort.md" %}
[insertion-sort.md](../../programming/python/algorithms/sorting/insertion-sort.md)
{% endcontent-ref %}
