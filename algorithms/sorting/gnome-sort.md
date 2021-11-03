# Gnome sort

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

#### Animation

{% embed url="https://blackbat13.github.io/visul2/sorting/gnome_sort/#array=%5B6%2C5%2C3%2C1%2C8%2C7%2C2%2C4%5D" %}

## Solution

<!-- TODO -->

### Pseudocode

```
procedure GnomeSort(n, A):
    1. i := 1
    2. While i <= n, do:
        3. If i = 1 or A[i] >= A[i - 1], then:
            4. i := i + 1
        5. else:
            6. Swap(A[i], A[i - 1])
            7. i := i - 1
```

### Complexity

$$O(n^2)$$ - square

## Implementation

### C++

{% content-ref url="../../programming/c++/algorithms/sorting/gnome-sort.md" %}
[gnome-sort.md](../../programming/c++/algorithms/sorting/gnome-sort.md)
{% endcontent-ref %}

### Python

{% content-ref url="../../programming/python/algorithms/sorting/gnome-sort.md" %}
[gnome-sort.md](../../programming/python/algorithms/sorting/gnome-sort.md)
{% endcontent-ref %}
