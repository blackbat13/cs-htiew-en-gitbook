# Cocktail sort

## Opis problemu

{% content-ref url="../../../../algorithms/sorting/cocktail-sort.md" %}
[cocktail-sort.md](../../../../algorithms/sorting/cocktail-sort.md)
{% endcontent-ref %}

## Implementation

```python
def cocktail_shaker_sort(array: list, n: int):
    for i in range(n//2+1):
        for j in range(i, n-i-1):
            if array[j] > array[j + 1]:
                array[j], array[j + 1] = array[j + 1], array[j]
        
        for j in range(n - 1 - i, i, -1):
            if array[j] < array[j - 1]:
                array[j], array[j - 1] = array[j - 1], array[j]


array = [7, 3, 0, 1, 5, 2, 5, 19, 10, 5]
n = 10

cocktail_shaker_sort(array, n)
    
print(array)
```

### Link do implementacji

{% embed url="https://ideone.com/C38hze" %}
Cocktail sort
{% endembed %}

### Opis implementacji

TODO
