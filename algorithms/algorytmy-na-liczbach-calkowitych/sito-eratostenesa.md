# Sito Eratostenesa

## Problem description

TODO

### Specification

#### Input:

* $$n$$ - liczba całkowita

#### Output:

* Wszystkie liczby pierwsze od $$1$$ do $$n$$ włącznie.

### Example

#### Input

```
n := 10
```

#### Output

$$2, 3, 5, 7$$ 

### Prezentacja

{% file src="../../.gitbook/assets/Sito Eratostenesa.pdf" %}
Prezentacja
{% endfile %}

## Solution

TODO

### Pseudocode

```
funkcja SitoEratostenesa(n):
    1. A[1..n] := tablica wypełniona wartościami true
    2. A[1] := false
    3. Od i := 2 do n wykonuj:
        4. Jeżeli A[i] = true, to:
            5. j := i * 2
            6. Dopóki j <= n, wykonuj:
                7. A[j] := false
                8. j := j + i
    9. Od i := 2 do n, wykonuj:
        10. Jeżeli A[i] = true, to:
            11. Wypisz i
```

### Complexity

TODO

## Implementation

### C++

{% content-ref url="../../programming/c++/algorithms/algorytmy-na-liczbach-calkowitych/sito-eratostenesa.md" %}
[sito-eratostenesa.md](../../programming/c++/algorithms/algorytmy-na-liczbach-calkowitych/sito-eratostenesa.md)
{% endcontent-ref %}

### Python

{% content-ref url="../../programming/python/algorithms/algorytmy-na-liczbach-calkowitych/sito-eratostenesa.md" %}
[sito-eratostenesa.md](../../programming/python/algorithms/algorytmy-na-liczbach-calkowitych/sito-eratostenesa.md)
{% endcontent-ref %}
