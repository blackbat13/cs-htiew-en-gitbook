# Znajdowanie lidera w zbiorze

## Problem description

TODO

### Specification

#### Input:

* $$n$$ - liczba naturalna, liczebność zbioru
* $$A[1..n]$$ - $$n-elementowy$$ zbiór liczb całkowitych, indeksowany od jedynki

#### Output:

* Lider podanego zbioru, lub -1, jeżeli lider nie istnieje.

{% hint style="info" %}
#### Lider zbioru

**Liderem **zbioru $$n-elementowego$$ nazywamy element, którego ilość wystąpień w zbiorze jest większa niż $$\frac{n}{2}$$.

Jeżeli taki element nie istnieje, to zbiór nie ma lidera.
{% endhint %}

### Example 1

#### Input:

```
n := 10
A := [4, 1, 4, 4, 2, 3, 4, 3, 4, 4]
```

**Wynik**: 4

{% hint style="info" %}
#### Wyjaśnienie

Najczęściej występującym elementem w powyższym zbiorze jest wartość $$4$$, która występuje dokładnie $$6$$ razy, co **jest wartością większą** od $$n/2=10/2=5$$.
{% endhint %}

### Example 2

#### Input:

```
n := 10
A := [4, 1, 4, 4, 2, 3, 4, 3, 4, 1]
```

**Wynik**: $$-1$$ (brak lidera)

{% hint style="info" %}
#### Wyjaśnienie

Najczęściej występującym elementem w powyższym zbiorze jest wartość $$4$$, która występuje dokładnie $$5$$ razy, co **nie jest** **wartością większą** od $$n/2=10/2=5$$.
{% endhint %}

## Solution

TODO

### Pseudocode

```
funkcja SzukajLidera(n, A)
    1. lider := 0
    2. ile := 0
    3. Od i := 1 do n, wykonuj:
        4. Jeżeli ile = 0, to:
            5. lider := A[i]
            6. ile := 1
        
        7. w przeciwnym przypadku, jeżeli lider = A[i]:
            8. ile := ile + 1
        
        9. w przeciwnym przypadku:
            10. ile := ile - 1
        
    11. ile := 0
    12. Od i := 1 do n, wykonuj:
        13. Jeżeli A[i] = lider, to:
            14. ile := ile + 1
        
    15. Jeżeli ile > n/2, to:
        16. Zwróć lider, zakończ
    
    17. w przeciwnym przypadku:
        18. Zwróć -1, zakończ
```

### Complexity

$$O(n)$$ - liniowa

## Implementation

### C++

{% content-ref url="../../programming/c++/algorithms/searching/znajdowanie-lidera-w-zbiorze.md" %}
[znajdowanie-lidera-w-zbiorze.md](../../programming/c++/algorithms/searching/znajdowanie-lidera-w-zbiorze.md)
{% endcontent-ref %}

### Python

{% content-ref url="../../programming/python/algorithms/searching/znajdowanie-lidera-w-zbiorze.md" %}
[znajdowanie-lidera-w-zbiorze.md](../../programming/python/algorithms/searching/znajdowanie-lidera-w-zbiorze.md)
{% endcontent-ref %}
