# Liczby Fibonacciego

## Problem description

{% content-ref url="../../../../algorithms/algorytmy-na-liczbach-calkowitych/liczby-fibonacciego.md" %}
[liczby-fibonacciego.md](../../../../algorithms/algorytmy-na-liczbach-calkowitych/liczby-fibonacciego.md)
{% endcontent-ref %}

## Wersja iteracyjna

### Implementation

```python
def fib(n: int) -> int:
    f1 = 1
    f2 = 1
    
    for i in range(3, n + 1):
        f3 = f1 + f2
        f1 = f2
        f2 = f3

    return f2


n = 10

result = fib(n)

print(f"fib({n}) = {result}")
```

### Link do implementacji

{% embed url="https://ideone.com/Y64Pew" %}
Liczby Fibonacciego - wersja iteracyjna
{% endembed %}

### Implementation descriptioni

TODO

## Wersja rekurencyjna

### Implementation

```python
def fib(n: int) -> int:
    if n <= 2:
        return 1
        
    return fib(n - 1) + fib(n - 2)


n = 10

result = fib(n)

print(f"fib({n}) = {result}")
```

### Link do implementacji

{% embed url="https://ideone.com/tdrBFE" %}
Liczby Fibonacciego - wersja rekurencyjna
{% endembed %}

### Implementation descriptioni

TODO

