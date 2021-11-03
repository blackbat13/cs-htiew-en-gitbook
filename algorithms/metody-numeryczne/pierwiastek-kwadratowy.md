# Pierwiastek kwadratowy

## Problem description

TODO

### Specification

#### Input

* $$n$$ - liczba rzeczywista.
* $$p$$ - liczba rzeczywista, dokładność.

#### Output

* $$\sqrt{n}$$ policzony z dokładnością $$p$$. 

### Example

TODO

## Solution - metoda Herona

TODO

### Pseudocode

```
funkcja MetodaHerona(n, p)
    1. x1 := n / 2
    2. x2 := (x1 + (n / x1)) / 2
    3. Dopóki |x2 - x1| > p, wykonuj:
        4. x1 := (x2 + (n / x2)) / 2
        3. Zamień(x1, x2)
    4. Zwróć x2
```

### Complexity

TODO

## Implementation

### C++

{% content-ref url="../../programming/c++/algorithms/metody-numeryczne/pierwiastek-kwadratowy.md" %}
[pierwiastek-kwadratowy.md](../../programming/c++/algorithms/metody-numeryczne/pierwiastek-kwadratowy.md)
{% endcontent-ref %}

### Python

{% content-ref url="../../programming/python/algorithms/metody-numeryczne/pierwiastek-kwadratowy.md" %}
[pierwiastek-kwadratowy.md](../../programming/python/algorithms/metody-numeryczne/pierwiastek-kwadratowy.md)
{% endcontent-ref %}
