# Rozkład na czynniki pierwsze

## Opis problemu

TODO

### Specyfikacja

#### Input

* $$n$$ - liczba naturalna, większa od zera

#### Wynik

* Rozkład liczby $$n$$ na czynniki pierwsze 

### Example

#### Input

```
n := 124
```

**Wynik**: $$2, 2, 31$$ 

## Solution

TODO

### Pseudocode

```
funkcja Rozklad(n):
    1. i := 2
    2. Dopóki n > 1, wykonuj:
        3. Jeżeli n mod i = 0, to:
            4. Wypisz i
            5. n := n div i
        6. W przeciwnym przypadku:
            7. i := i + 1
```

{% hint style="info" %}
**mod** oznacza resztę z dzielenia

**div** oznacza dzielenie całkowite
{% endhint %}

### Schemat blokowy

TODO

## Implementation

### C++

{% content-ref url="../../programming/c++/algorithms/algorytmy-na-liczbach-calkowitych/rozklad-na-czynniki-pierwsze.md" %}
[rozklad-na-czynniki-pierwsze.md](../../programming/c++/algorithms/algorytmy-na-liczbach-calkowitych/rozklad-na-czynniki-pierwsze.md)
{% endcontent-ref %}

### Python

{% content-ref url="../../programming/python/algorithms/algorytmy-na-liczbach-calkowitych/rozklad-na-czynniki-pierwsze.md" %}
[rozklad-na-czynniki-pierwsze.md](../../programming/python/algorithms/algorytmy-na-liczbach-calkowitych/rozklad-na-czynniki-pierwsze.md)
{% endcontent-ref %}
