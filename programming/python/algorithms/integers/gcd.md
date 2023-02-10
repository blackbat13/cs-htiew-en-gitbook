---
description: Największy Wspólny Dzielnik
---

# GCD

## Problem description

{% content-ref url="../../../../algorithms/integers/gcd.md" %}
[gcd.md](../../../../algorithms/integers/gcd.md)
{% endcontent-ref %}

## GCD with subtraction

### Implementation

{% code overflow="wrap" lineNumbers="true" %}
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
{% endcode %}

### Link do implementacji

{% embed url="https://ideone.com/OfD6kn" %}
NWD z odejmowaniem
{% endembed %}

## Iterative GCD with modulo

### Implementation

{% code overflow="wrap" lineNumbers="true" %}
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
{% endcode %}

### Link do implementacji

{% embed url="https://ideone.com/02yQ0m" %}
Algorytm Euklidesa - wersja iteracyjna
{% endembed %}

## Recursive GCD with modulo

### Implementation

{% code overflow="wrap" lineNumbers="true" %}
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
{% endcode %}

### Link do implementacji

{% embed url="https://ideone.com/b8Zfab" %}
Algorytm Euklidesa - wersja rekurencyjna
{% endembed %}
