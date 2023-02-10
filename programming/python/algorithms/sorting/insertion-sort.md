# Sortowanie przez wstawianie

## Problem description

{% content-ref url="../../../../algorithms/sorting/insertion-sort.md" %}
[insertion-sort.md](../../../../algorithms/sorting/insertion-sort.md)
{% endcontent-ref %}

## Implementation

{% code overflow="wrap" lineNumbers="true" %}
```python
def insertion_sort(array: list):
    for i in range(1, len(array)):
        j = i
        
        while j > 0 and array[j] < array[j - 1]:
            array[j], array[j - 1] = array[j - 1], array[j]
            j -= 1


array = [7, 3, 0, 1, 5, 2, 5, 19, 10, 5]

insertion_sort(array)

print(array)
```
{% endcode %}

### Link do implementacji

{% embed url="https://ideone.com/ublO4B" %}
Sortowanie przez wstawianie
{% endembed %}
