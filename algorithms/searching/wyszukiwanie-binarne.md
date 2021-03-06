# Wyszukiwanie binarne

## Problem description

TODO

### Specification

#### Input:

* $$n$$ - liczba naturalna, ilość elementów w tablicy
* $$A[1..n]$$ - posortowana niemalejąco tablica $$n$$ wartości całkowitych
* $$k$$ - liczba całkowita, szukana wartość

#### Output:

* Indeks wartości $$k$$ w tablicy $$A$$, lub $$-1$$ jeżeli tej wartości nie ma w tablicy

### Example

TODO

## Iterative solution

TODO

### Pseudocode

```
funkcja SzukajBinIter(n, A, k)
    1. ind := -1
    2. pocz := 1
    3. kon := n
    4. Dopóki pocz <= kon, wykonuj:
        5. srodek := (pocz + kon) div 2
        6. Jeżeli k = A[srodek], to:
            7. ind := srodek
            8. Wyjdź z pętli
        
        9. Jeżeli k < A[srodek], to:
            10. kon := srodek - 1
        
        11. W przeciwnym przypadku:
            12. pocz := srodek + 1

    13. Zwróć ind, zakończ
```

### Complexity

$$O(\log n)$$ - logarytmiczna

## Recursive solution

TODO

### Pseudocode

```
funkcja SzukajBinRek(A, k, pocz, kon)
    1. Jeżeli pocz > kon, to:
        2. Zwróć -1, zakończ
    
    3. srodek := (pocz + kon) div 2
    4. Jeżeli k == A[srodek], to:
        5. Zwróć srodek, zakończ
    
    6. Jeżeli k < A[srodek], to:
        7. Zwróć SzukajBinRek(A, k, pocz, srodek-1)
    
    8. W przeciwnym przypadku:
        9. Zwróć SzukajBinRek(A, k, srodek+1, kon)
```

{% hint style="info" %}
**div **oznacza dzielenie całkowite
{% endhint %}

### Complexity 

$$O(\log n)$$ - logarytmiczna

## Implementation

### C++

{% content-ref url="../../programming/c++/algorithms/searching/wyszukiwanie-binarne.md" %}
[wyszukiwanie-binarne.md](../../programming/c++/algorithms/searching/wyszukiwanie-binarne.md)
{% endcontent-ref %}

### Python

{% content-ref url="../../programming/python/algorithms/searching/wyszukiwanie-binarne.md" %}
[wyszukiwanie-binarne.md](../../programming/python/algorithms/searching/wyszukiwanie-binarne.md)
{% endcontent-ref %}

### Blockly

{% content-ref url="../../programming/blockly/algorithms/searching/wyszukiwanie-binarne.md" %}
[wyszukiwanie-binarne.md](../../programming/blockly/algorithms/searching/wyszukiwanie-binarne.md)
{% endcontent-ref %}
