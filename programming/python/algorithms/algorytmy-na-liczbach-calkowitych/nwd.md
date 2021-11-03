---
description: Największy Wspólny Dzielnik
---

# NWD

## Problem description

{% content-ref url="../../../../algorithms/algorytmy-na-liczbach-calkowitych/algorytm-euklidesa.md" %}
[algorytm-euklidesa.md](../../../../algorithms/algorytmy-na-liczbach-calkowitych/algorytm-euklidesa.md)
{% endcontent-ref %}

## Algorytm NWD z odejmowaniem

### Implementation

```python
def gcd(a: int, b: int) -> int:
    while a != b:
        if a > b:
            a -= b
        else:
            b -= a

    return a


a = 32
b = 12

result = gcd(a, b)

print(f"GCD({a}, {b}) = {result}")
```

### Link do implementacji

{% embed url="https://ideone.com/OfD6kn" %}
NWD z odejmowaniem
{% endembed %}

### Implementation descriptioni

TODO

## Algorytm Euklidesa - wersja iteracyjna

### Implementation

```python
def gcd(a: int, b: int) -> int:
    while b != 0:
        b2 = b
        b = a % b
        a = b2

    return a


a = 32
b = 12

result = gcd(a, b)

print(f"GCD({a},{b}) = {result}")
```

### Link do implementacji

{% embed url="https://ideone.com/02yQ0m" %}
Algorytm Euklidesa - wersja iteracyjna
{% endembed %}

### Implementation descriptioni

TODO

## Algorytm Euklidesa - wersja rekurencyjna

### Implementation

```python
def gcd(a: int, b: int) -> int:
    if b == 0:
        return a
        
    return gcd(b, a % b)


a = 32
b = 12

result = gcd(a, b)

print(f"GCD({a},{b}) = {result}")
```

### Link do implementacji

{% embed url="https://ideone.com/b8Zfab" %}
Algorytm Euklidesa - wersja rekurencyjna
{% endembed %}

### Implementation descriptioni

TODO
