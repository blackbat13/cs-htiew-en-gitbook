# Test doskonałości

## Problem description

{% content-ref url="../../../../algorithms/algorytmy-na-liczbach-calkowitych/test-doskonalosci.md" %}
[test-doskonalosci.md](../../../../algorithms/algorytmy-na-liczbach-calkowitych/test-doskonalosci.md)
{% endcontent-ref %}

## Implementation

```python
def is_perfect(n: int) -> bool:
    sum = 0
    
    for i in range(1, n):
        if n % i == 0:
            sum += i

    return sum == n


n = 6

if is_perfect(n):
    print(f'{n} is a perfect number')
else:
    print(f'{n} is not a perfect number')
```

### Link do implementacji

{% embed url="https://ideone.com/4EALRV" %}
Test doskonałości
{% endembed %}

### Implementation descriptioni

TODO
