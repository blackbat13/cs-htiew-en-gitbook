# Wyszukiwanie minimum i maksimum

## Opis problemu

TODO

## Wyszukiwanie wartości maksymalnej w tablicy

### Opis problemu

TODO

### Specyfikacja

#### Input:

* $$n$$ - liczba naturalna, liczba elementów w tablicy
* $$A[1..n]$$ - tablica $$n$$ wartości całkowitych

#### Wynik:

* Największa wartość z tablicy $$A$$

### Example

#### Input

```
n := 8
A := [6, 5, 3, 1, 8, 7, 2, 4]
```

**Wynik**: $$8$$ 

### Animacja

{% embed url="https://blackbat13.github.io/visul2/searching/find_max/#array=%5B6%2C5%2C3%2C1%2C8%2C7%2C2%2C4%5D" %}
Wyszukiwanie maksimum
{% endembed %}

### Solution

TODO

### Pseudocode

```
funkcja SzukajMaks(n, A):
    1. maks := A[1]
    2. Od i := 2 do n, wykonuj:
        3. Jeżeli maks < A[i], to:
            4. maks := A[i]

    5. Zwróć maks, zakończ
```

### Complexity

$$O(n)$$ - liniowa

## Wyszukiwanie indeksu wartości maksymalnej w tablicy

### Opis problemu

TODO

### Specyfikacja

#### Input:

* $$n$$ - liczba naturalna, ilość elementów w tablicy
* $$A[1..n]$$ - tablica $$n$$ wartości całkowitych

#### Wynik:

* Indeks największej wartości z tablicy $$A$$ 

### Example

#### Input

```
n := 8
A := [6, 5, 3, 1, 8, 7, 2, 4]
```

**Wynik**: $$5$$ 

{% hint style="info" %}
**Wyjaśnienie**

Największa wartość w tablicy to $$8$$. Wartość ta znajduje się na pozycji piątej.
{% endhint %}

### Solution

TODO

### Pseudocode

```
funkcja SzukajIndeksMaks(n, A):
    1. maks := A[1]
    2. ind := 1
    3. Od i := 2 do n, wykonuj:
        4. Jeżeli maks < A[i], to:
            5. maks := A[i]
            6. ind := i
    
    7. Zwróć ind, zakończ    
```

### Complexity

$$O(n)$$ - liniowa

## Implementation

### C++

{% content-ref url="../../programming/c++/algorithms/searching/wyszukiwanie-minimum-i-maksimum.md" %}
[wyszukiwanie-minimum-i-maksimum.md](../../programming/c++/algorithms/searching/wyszukiwanie-minimum-i-maksimum.md)
{% endcontent-ref %}

### Python

{% content-ref url="../../programming/python/algorithms/searching/wyszukiwanie-minimum-i-maksimum.md" %}
[wyszukiwanie-minimum-i-maksimum.md](../../programming/python/algorithms/searching/wyszukiwanie-minimum-i-maksimum.md)
{% endcontent-ref %}

### Blockly

{% content-ref url="../../programming/blockly/algorithms/searching/wyszukiwanie-minimum-i-maksimum.md" %}
[wyszukiwanie-minimum-i-maksimum.md](../../programming/blockly/algorithms/searching/wyszukiwanie-minimum-i-maksimum.md)
{% endcontent-ref %}
