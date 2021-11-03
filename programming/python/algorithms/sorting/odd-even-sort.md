# Odd-Even sort

## Problem description

{% content-ref url="../../../../algorithms/sorting/odd-even-sort.md" %}
[odd-even-sort.md](../../../../algorithms/sorting/odd-even-sort.md)
{% endcontent-ref %}

## Implementation

```python
def odd_even_sort(array: list):
    for i in range(len(array)):
        if i % 2 == 1:
            for j in range(2, len(array), 2):
                if array[j] < array[j - 1]:
                    array[j], array[j - 1] = array[j - 1], array[j]
        else:
            for j in range(1, len(array), 2):
                if array[j] < array[j - 1]:
                    array[j], array[j - 1] = array[j - 1], array[j]


array = [7, 3, 0, 1, 5, 2, 5, 19, 10, 5]

odd_even_sort(array)

print(array)
```

### Link do implementacji

{% embed url="https://ideone.com/r1Bb5H" %}
Odd-Even sort
{% endembed %}

### Implementation descriptioni

TODO

