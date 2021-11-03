---
description: Selection sort
---

# Selection sort

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
n := 10
A := [8, 5, 2, 6, 9, 3, 1, 4, 0, 7]
```

#### Animation 1

![By Joestape89, CC BY-SA 3.0, https://commons.wikimedia.org/w/index.php?curid=3330231](../../.gitbook/assets/Selection-Sort-Animation.gif)

#### Animation 2

{% embed url="https://blackbat13.github.io/visul2/sorting/selection_sort/#array=%5B8%2C5%2C2%2C6%2C9%2C3%2C1%2C4%2C0%2C7%5D" %}

## Solution

TODO

### Pseudocode

```
function FindMin(p, k, A):
    1. min := A[p]
    2. min_ind := p
    3. For i := p + 1 to k, do:
        4. If A[i] < min, then:
            5. min := A[i]
            6. min_ind := i
    7. Return min_ind

procedure SortWybier(A, n):
    1. For i := 1 to n-1, do:
        2. min_ind := FindMin(i, n, A)
        3. Swap(A[i], A[min_ind])
```

### Complexity

$$O(n^2)$$ - square

## Implementation

### C++

{% content-ref url="../../programming/c++/algorithms/sorting/selection-sort.md" %}
[selection-sort.md](../../programming/c++/algorithms/sorting/selection-sort.md)
{% endcontent-ref %}

### Python

{% content-ref url="../../programming/python/algorithms/sorting/selection-sort.md" %}
[selection-sort.md](../../programming/python/algorithms/sorting/selection-sort.md)
{% endcontent-ref %}

### Blockly

{% content-ref url="../../programming/blockly/algorithms/sorting/selection-sort.md" %}
[selection-sort.md](../../programming/blockly/algorithms/sorting/selection-sort.md)
{% endcontent-ref %}
