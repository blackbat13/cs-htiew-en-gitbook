---
description: Sprawdzanie, czy wyraz jest palindromem
---

# Palindrom

## Problem description

TODO

{% hint style="info" %}
**Palindrom **to wyraz, który czytany od lewej do prawej i od prawej do lewej jest taki sam.
{% endhint %}

### Specification

#### Input:

* $$n$$ - długość tekstu
* $$tekst[1..n]$$ - ciąg znaków o długości $$n$$, numerowanych od jedynki 

#### Output:

* $$True$$ - jeżeli $$tekst$$ jest palindromem
* $$False$$ - w przeciwnym przypadku

### Example 1

#### Input

```
n := 5
tekst := "kajak"
```

#### Output: $$True$$ 

{% hint style="info" %}
**Wyjaśnienie**

Wyraz **kajak** czytany od tyłu to **kajak**, jest on więc palindromem.
{% endhint %}

### Example 2

#### Input

```
n := 4
tekst := "tama"
```

**Wynik**: $$False$$ 

{% hint style="info" %}
**Wyjaśnienie**

Wyraz **tama** czytany od tyłu to **amat**, nie jest on więc palindromem.
{% endhint %}

## Solution

TODO

### Pseudocode

```
funkcja czyPalindrom(n, tekst):
    1. srodek := n div 2
    2. Od i := 1 do srodek, wykonuj:
        3. Jeżeli tekst[i] != tekst[n-i+1], to:
            4. Zwróć False, zakończ
    5. Zwróć True, zakończ
```

### Complexity

$$O(n/2)\to O(n)$$ - liniowa 

## Implementation

### C++

{% content-ref url="../../programming/c++/algorithms/tekstowe/palindrom.md" %}
[palindrom.md](../../programming/c++/algorithms/tekstowe/palindrom.md)
{% endcontent-ref %}

### Python

{% content-ref url="../../programming/python/algorithms/tekstowe/palindrom.md" %}
[palindrom.md](../../programming/python/algorithms/tekstowe/palindrom.md)
{% endcontent-ref %}

