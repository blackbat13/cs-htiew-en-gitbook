# Szybkie potęgowanie

## Problem description

{% content-ref url="../../../../algorithms/metody-numeryczne/szybkie-potegowanie.md" %}
[szybkie-potegowanie.md](../../../../algorithms/metody-numeryczne/szybkie-potegowanie.md)
{% endcontent-ref %}

## Recursive solution

```python
def fast_exp_rec(a: int, n : int) -> int:
    if n == 1:
        return a
        
    if n % 2 == 1:
        return fast_exp_rec(a, n // 2) ** 2 * a
    else:
        return fast_exp_rec(a, n // 2) ** 2

 
a = 2
n = 10

result = fast_exp_rec(a, n)

print(f"{a}^{n} = {result}")
```

### Link do implementacji

{% embed url="https://ideone.com/3i2qdR" %}
Szybkie potęgowanie - wersja rekurencyjna
{% endembed %}

### Implementation descriptioni

TODO

## Iterative solution

```python
def fast_exp_iter(a: int, n: int) -> int:
    w = 1
    
    while n > 0:
        if n % 2 == 1:
            w *= a

        a *= a
        n = n // 2

    return w


a = 2
n = 10

result = fast_exp_iter(a, n)

print(f"{a}^{n} = {result}")
```

### Link do implementacji

{% embed url="https://ideone.com/pSGzrA" %}
Szybkie potęgowanie - wersja iteracyjna
{% endembed %}

### Implementation descriptioni

TODO
