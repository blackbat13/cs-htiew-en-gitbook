# Liczby Fibonacciego

## Problem description

TODO

### Specification

#### Input

* $$n$$ - liczba naturalna, większa od zera

#### Output

* $$n$$-ta liczba Fibonacciego

### Example

#### Input

```
n := 10
```

**Wynik**: $$55$$ 

{% hint style="info" %}
**Wyjaśnienie**

Pierwszych kolejnych dziesięć liczb Fibonacciego to: $$1, 1, 2, 3, 5, 8, 13, 21, 34, 55$$ 
{% endhint %}

## Recursive solution

TODO

### Pseudocode

```
funkcja Fib(n):
    1. Jeżeli n <= 2, to:
        2. Zwróć 1 i zakończ
    3. Zwróć Fib(n - 1) + Fib(n - 2) i zakończ
```

### Schemat blokowy

TODO

## Iterative solution

TODO

### Pseudocode

```
funkcja Fib(n):
    1. f1 := 1
    2. f2 := 1
    3. Od i := 3 do n + 1, wykonuj:
        4. f3 := f1 + f2
        5. f1 := f2
        6. f2 := f3
    7. Zwróć f2
```

### Schemat blokowy

TODO

## Implementation

### C++

{% content-ref url="../../programming/c++/algorithms/algorytmy-na-liczbach-calkowitych/liczby-fibbonacciego.md" %}
[liczby-fibbonacciego.md](../../programming/c++/algorithms/algorytmy-na-liczbach-calkowitych/liczby-fibbonacciego.md)
{% endcontent-ref %}

### Python

{% content-ref url="../../programming/python/algorithms/algorytmy-na-liczbach-calkowitych/liczby-fibonacciego.md" %}
[liczby-fibonacciego.md](../../programming/python/algorithms/algorytmy-na-liczbach-calkowitych/liczby-fibonacciego.md)
{% endcontent-ref %}
