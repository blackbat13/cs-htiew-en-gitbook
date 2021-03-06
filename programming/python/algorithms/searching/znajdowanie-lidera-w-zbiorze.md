# Znajdowanie lidera w zbiorze

## Problem description

{% content-ref url="../../../../algorithms/searching/znajdowanie-lidera-w-zbiorze.md" %}
[znajdowanie-lidera-w-zbiorze.md](../../../../algorithms/searching/znajdowanie-lidera-w-zbiorze.md)
{% endcontent-ref %}

## Implementation

```python
def count_occurrences(element: int, array: list) -> int:
    count = 0
    
    for el in array:
        if el == element:
            count += 1

    return count


def find_majority(array: list) -> int:
    counter = 0
    current_candidate = 0
    
    for el in array:
        if counter == 0:
            current_candidate = el
            counter = 1
        else:
            if el == current_candidate:
                counter += 1
            else:
                counter -= 1

    if count_occurrences(current_candidate, array) >= len(array) / 2:
        return current_candidate
    else:
        return -1


array = [1, 2, 5, 5, 7, 5, 5, 10, 5, 5]

majority = find_majority(array)

print(majority)
```

### Link do implementacji

{% embed url="https://ideone.com/9kFDlI" %}
Znajdowanie lidera w zbiorze
{% endembed %}

### Implementation descriptioni

TODO
