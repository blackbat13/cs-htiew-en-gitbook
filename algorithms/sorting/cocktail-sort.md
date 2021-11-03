# Cocktail sort

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

{% embed url="https://blackbat13.github.io/visul2/sorting/cocktail_shaker_sort/#array=%5B6%2C5%2C3%2C1%2C8%2C7%2C2%2C4%5D" %}

## Solution

TODO

### Pseudocode

```
procedure CocktailSort(n, A):
    1. For i := 1 to n div 2, do:
        2. For j := i to n - i, do:
            3. If A[j] > A[j + 1], then:
                4. Swap(A[j], A[j + 1])
        5. For j := n - i downto i + 1, do:
            6. If A[j] < A[j - 1], then:
                7. Swap(A[j], A[j - 1]
```

{% hint style="info" %}
**div** stands for integer division
{% endhint %}

### Complexity

TODO

## Implementation

### C++

{% content-ref url="../../programming/c++/algorithms/sorting/cocktail-sort.md" %}
[cocktail-sort.md](../../programming/c++/algorithms/sorting/cocktail-sort.md)
{% endcontent-ref %}

### Python

{% content-ref url="../../programming/python/algorithms/sorting/cocktail-sort.md" %}
[cocktail-sort.md](../../programming/python/algorithms/sorting/cocktail-sort.md)
{% endcontent-ref %}
