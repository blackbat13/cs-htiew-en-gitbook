# Counting sort

## Problem description

<!-- TODO -->

### Specification

#### Input:

* $$n$$ - natural number, number of elements in the array
* $$A[1..n]$$ - array of $$n$$ integers

#### Output:

* Array $$A$$ sorted in ascending order 

### Example

TODO

## Solution

<!-- TODO -->

### Pseudocode

```
procedure CountingSort(A, n, m):
    1. counters := array [1..m] filled with zeroes
    2. For i := 1 to n, do:
        3. counters[A[i]] := counters[A[i]] + 1
    4. position := 1
    5. For i := 1 to m, do:
        6. For j := 1 to counters[i], do:
            7. A[position] := i
            8. position := position + 1  
    9. Return A
```

### Complexity

$$O(n+m)$$ - linear

## Implementation

### C++

{% content-ref url="../../programming/c++/algorithms/sorting/counting-sort.md" %}
[counting-sort.md](../../programming/c++/algorithms/sorting/counting-sort.md)
{% endcontent-ref %}

### Python

{% content-ref url="../../programming/python/algorithms/sorting/counting-sort.md" %}
[counting-sort.md](../../programming/python/algorithms/sorting/counting-sort.md)
{% endcontent-ref %}

### Blockly

{% content-ref url="../../programming/blockly/algorithms/sorting/counting-sort.md" %}
[counting-sort.md](../../programming/blockly/algorithms/sorting/counting-sort.md)
{% endcontent-ref %}
