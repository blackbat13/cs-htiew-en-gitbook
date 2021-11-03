# Algorytm Euklidesa

## Problem description

TODO

### Specification

#### Input

* $$a, b$$ - liczby naturalne, większe od zera

#### Output

* $$NWD(a,b)$$ - największy wspólny dzielnik liczb $$a$$ i $$b$$ 

### Example

#### Input

```
a := 32
b := 12
```

**Wynik**: $$4$$ 

{% hint style="info" %}
**Wyjaśnienie**

Dzielnikami liczby $$32$$ są: $$1, 2, 4, 8, 16, 32$$

Dzielnikami liczby $$12$$ są: 1, 2, 3, 4, 6, 12

Wspólnymi dzielnikami są więc: $$1, 2, 4$$ 

Największy z nich to właśnie $$4$$.
{% endhint %}

## Wersja z odejmowaniem

TODO

### Pseudocode

```
funkcja NWD(a, b):
    1. Dopóki a != b, wykonuj:
        2. Jeżeli a > b, to:
            3. a := a - b
        4. W przeciwnym przypadku:
            5. b := b - a
    6. Zwróć a
```

### Schemat blokowy

TODO

## Wersja z modulo - iteracyjna

TODO

### Pseudocode

```
funkcja NWD(a, b):
    1. Dopóki b != 0, wykonuj:
        2. b2 := b
        3. b := a mod b
        4. a := b2
    5. Zwróc a
```

{% hint style="info" %}
**mod** oznacza resztę z dzielenia
{% endhint %}

### Schemat blokowy

TODO

## Wersja z modulo - rekurencyjna

TODO

### Pseudocode

```
funkcja NWD(a, b):
    1. Jeżeli b = 0, to:
        2. Zwróć a i zakończ
    3. Zwróć NWD(b, a mod b) i zakończ
```

### Schemat blokowy

TODO

## Implementation

### C++

{% content-ref url="../../programming/c++/algorithms/algorytmy-na-liczbach-calkowitych/nwd.md" %}
[nwd.md](../../programming/c++/algorithms/algorytmy-na-liczbach-calkowitych/nwd.md)
{% endcontent-ref %}

### Python

{% content-ref url="../../programming/python/algorithms/algorytmy-na-liczbach-calkowitych/nwd.md" %}
[nwd.md](../../programming/python/algorithms/algorytmy-na-liczbach-calkowitych/nwd.md)
{% endcontent-ref %}

### Blockly

{% content-ref url="../../programming/blockly/algorithms/algorytmy-na-liczbach-calkowitych/nwd.md" %}
[nwd.md](../../programming/blockly/algorithms/algorytmy-na-liczbach-calkowitych/nwd.md)
{% endcontent-ref %}

