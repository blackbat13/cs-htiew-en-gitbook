# Prime factors

## Problem description

{% content-ref url="../../../../algorithms/integers/prime-factors.md" %}
[prime-factors.md](../../../../algorithms/integers/prime-factors.md)
{% endcontent-ref %}

## Implementation

{% code overflow="wrap" lineNumbers="true" %}
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
{% endcode %}

### Link do implementacji

{% embed url="https://ideone.com/Kpj2pe" %}
Rozkład na czynniki pierwsze
{% endembed %}
