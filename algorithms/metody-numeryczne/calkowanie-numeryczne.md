# Całkowanie numeryczne

## Problem description

Hasło "całkowanie numeryczne" może brzmieć strasznie, ale samo pojęcie jest dość proste do zrozumienia. To nic innego, niż policzenie pola pod wykresem funkcji w zadanym przedziale. Oczywiście w ogólności to zadanie jest dość skomplikowane obliczeniowo, dlatego tutaj skupimy się na przybliżeniu tej wartości.

Wyróżniamy dwie podstawowe metody: metodę prostokątów i metodę trapezów.

### Specification

#### Input

* $$f(x)$$  - funkcja, której wykres nas interesuje
* $$a$$ - liczba rzeczywista, początek przedziału
* $$b$$ - liczba rzeczywista, koniec przedziału

#### Output

* $$p$$ - przybliżona wartość pola pod wykresem funkcji $$f(x)$$ w przedziale $$[a,b]$$

## Solution - metoda prostokątów

TODO

Idea tej metody jest prosta: podzielmy pole pod wykresem funkcji na prostokąty i policzmy ich pole.

### Pseudocode

```
funkcja MetodaProstokatow(f, a, b):
    1. p := 0
    2. n := 1000
    3. sz := (b - a) / n
    4. c := a + sz
    
    5. Dopóki c <= b, wykonuj:
        6. wys := f(c)
        7. p := p + sz * wys
        8. c := c + sz
        
    9. Zwróć p
```

### Complexity

TODO

## Solution - metoda trapezów

TODO

### Pseudocode

TODO

### Complexity

TODO

## Implementation

### C++

{% content-ref url="../../programming/c++/algorithms/metody-numeryczne/calkowanie-numeryczne.md" %}
[calkowanie-numeryczne.md](../../programming/c++/algorithms/metody-numeryczne/calkowanie-numeryczne.md)
{% endcontent-ref %}

### Python

{% content-ref url="../../programming/python/algorithms/metody-numeryczne/calkowanie-numeryczne.md" %}
[calkowanie-numeryczne.md](../../programming/python/algorithms/metody-numeryczne/calkowanie-numeryczne.md)
{% endcontent-ref %}
