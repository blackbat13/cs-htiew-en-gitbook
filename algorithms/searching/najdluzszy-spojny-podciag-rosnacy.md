# Najdłuższy spójny podciąg rosnący

## Problem description

TODO

### Specification

#### Input

* $$n$$ - liczba elementów tablicy
* $$tab[1..n]$$ - tablica zawierająca $$n$$ liczb

#### Output

* Długość najdłuższego spójnego podciągu rosnącego w tablicy $$tab$$ 

### Example

#### Input

```
n := 10
tab := [4, 9, 7, 2, 4, 7, 9, 3, 8, 6]
```

#### Output

$$4$$ 

{% hint style="info" %}
**Wyjaśnienie**

W podanej tablicy mamy kilka spójnych podciągów rosnących. Wypiszmy wszystkie pełne (tzn. takie, których już nie można powiększyć):

* 4, 9
* 7
* 2, 4, 7, 9
* 3, 8
* 6

Jak widać najdłuższy z nich ma długość równą $$4$$ i jest to podciąg: 2, 4, 7, 9.
{% endhint %}

## Solution

TODO

Zastanówmy się na początku, jak podeszlibyśmy do tego problemu na papierze. Mamy dany pewien ciąg liczb i chcemy odnaleźć najdłuższy spójny podciąg rosnący. To, co możemy zrobić, to wypisać wszystkie pełne spójne ciągi rosnące. Jak to zrobić? Pomysł jest prosty. Najpierw zapisujemy sobie pierwszą wartość z ciągu. Następnie idziemy od lewej do prawej, liczba po liczbie, zaczynając od drugiej w kolejności. Porównujemy ją z ostatnią zapisaną. Jeżeli jest większa, to dopisujemy ją obok (dopisując do podciągu). Jeżeli jest mniejsza lub równa, to zapisujemy ją poniżej (rozpoczynając nowy podciąg). 

{% hint style="info" %}
Dla lepszego zrozumienia spróbuj wykonać opisaną procedurę na kilku przykładach.
{% endhint %}

### Pseudocode

```
funkcja najdluzszySpojnyPodciagRosnacy(n, tab):
    1. maks := 1
    2. dlugosc := 1
    3. Od i := 2 do n, wykonuj:
        4. Jeżeli tab[i] > tab[i - 1], to:
            5. dlugosc := dlugosc + 1
            6. Jeżeli dlugosc > maks, to:
                7. maks := dlugosc
        8. W przeciwnym przypadku:
            9. dlugosc := 1
    10. Zwróć maks
```

### Complexity

$$O(n)$$ - liniowa

## Implementation

### C++

{% content-ref url="../../programming/c++/algorithms/searching/najdluzszy-spojny-podciag-rosnacy.md" %}
[najdluzszy-spojny-podciag-rosnacy.md](../../programming/c++/algorithms/searching/najdluzszy-spojny-podciag-rosnacy.md)
{% endcontent-ref %}

### Python

{% content-ref url="../../programming/python/algorithms/searching/najdluzszy-spojny-podciag-rosnacy.md" %}
[najdluzszy-spojny-podciag-rosnacy.md](../../programming/python/algorithms/searching/najdluzszy-spojny-podciag-rosnacy.md)
{% endcontent-ref %}

