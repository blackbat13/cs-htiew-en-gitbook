# Rozkład na czynniki pierwsze

## Problem description

{% content-ref url="../../../../algorithms/algorytmy-na-liczbach-calkowitych/rozklad-na-czynniki-pierwsze.md" %}
[rozklad-na-czynniki-pierwsze.md](../../../../algorithms/algorytmy-na-liczbach-calkowitych/rozklad-na-czynniki-pierwsze.md)
{% endcontent-ref %}

## Implementation

```python
def distribute(n: int) -> list:
    prime_factors = []
    i = 2
    
    while n > 1:
        if n % i == 0:
            prime_factors.append(i)
            n /= i
        else:
            i += 1

    return prime_factors


n = 124

print(f"Prime factors of {n}: {distribute(n)}")
```

### Link do implementacji

{% embed url="https://ideone.com/Kpj2pe" %}
Rozkład na czynniki pierwsze
{% endembed %}

### Implementation descriptioni

TODO
