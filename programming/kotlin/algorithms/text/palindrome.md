# Palindrom

## Problem description

{% content-ref url="../../../../algorithms/text/palindrome.md" %}
[palindrome.md](../../../../algorithms/text/palindrome.md)
{% endcontent-ref %}

## Implementation

```python
def is_palindrome(a: str) -> bool:
    return a == a[::-1]


a = "kajak"

if is_palindrome(a):
    print(f'{a} jest palindromem')
else:
    print(f'{a} nie jest palindromem')
```

### Link do implementacji

{% embed url="https://ideone.com/nsapMq" %}
Test palindromu
{% endembed %}

### Implementation description

TODO
