# Wydawanie reszty

## Problem description

TODO

### Specification

#### Input

* $$n$$ - liczba naturalna, ilość dostępnych nominałów
* $$nom[1..n]$$ - tablica dostępnych nominałów (liczb całkowitych) o rozmiarze $$n$$ 
* $$kw$$ - liczba naturalna, kwota do wydania

#### Output

* Minimalna liczba potrzebnych monet/banknotów do wydania kwoty $$kw$$ przy użyciu nominałów $$nom$$.

### Example

TODO

## Greedy solution

TODO

### Pseudocode

```
funkcja Reszta(n, nom, kw):
    1. Sortujemy tablicę nom od największych do najmniejszych (malejąco)
    2. wynik := 0
    3. Od i := 1 do n, wykonuj:
        4. Dopóki kw >= nom[i], to:
            5. kw := kw - nom[i]
            6. wynik := wynik + 1
            
    7. Zwróć wynik
```

#### Optymalizacja

```
funkcja Reszta(n, nom, kw):
    1. Sortujemy tablicę nom od największych do najmniejszych (malejąco)
    2. wynik := 0
    3. Od i := 1 do n, wykonuj:
        4. Jeżeli kw >= nom[i], to:
            5. wynik := wynik + kw div nom[i]
            6. kw := kw mod nom[i]
            
    7. Zwróć wynik
```

{% hint style="info" %}
**div** oznacza dzielenie całkowite

**mod** oznacza resztę z dzielenia
{% endhint %}

### Complexity

$$O(n)$$ - liniowa

## Dynamic solution

TODO

### Pseudocode

TODO

### Complexity

TODO

## Implementation

### C++

{% content-ref url="../../programming/c++/algorithms/algorytmy-na-liczbach-calkowitych/wydawanie-reszty.md" %}
[wydawanie-reszty.md](../../programming/c++/algorithms/algorytmy-na-liczbach-calkowitych/wydawanie-reszty.md)
{% endcontent-ref %}

### Python

{% content-ref url="../../programming/python/algorithms/algorytmy-na-liczbach-calkowitych/zachlanne-wydawanie-reszty.md" %}
[zachlanne-wydawanie-reszty.md](../../programming/python/algorithms/algorytmy-na-liczbach-calkowitych/zachlanne-wydawanie-reszty.md)
{% endcontent-ref %}
