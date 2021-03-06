# Bubble sort

## Problem description

{% content-ref url="../../../../algorithms/sorting/bubble-sort.md" %}
[bubble-sort.md](../../../../algorithms/sorting/bubble-sort.md)
{% endcontent-ref %}

## Wersja standardowa

### Implementation

```python
def bubble_sort(array: list):
    for i in range(0, len(array) - 2):
        for j in range(len(array) - 1, i, -1):
            if array[j - 1] > array[j]:
                array[j], array[j - 1] = array[j-1], array[j]


array = [7, 3, 0, 1, 5, 2, 5, 19, 10, 5]

bubble_sort(array)

print(array)
```

### Link do implementacji

{% embed url="https://ideone.com/1WKZb9" %}
Bubble sort - wersja standardowa
{% endembed %}

### Implementation descriptioni

TODO

## Wersja zoptymalizowana

### Implementation

```python
def bubble_sort(array: list):
    for i in range(0, len(array) - 2):
        swap = False
        
        for j in range(len(array) - 1, i, -1):
            if array[j - 1] > array[j]:
                array[j], array[j - 1] = array[j-1], array[j]
                swap = True

        if not swap:
            return


array = [7, 3, 0, 1, 5, 2, 5, 19, 10, 5]

bubble_sort(array)

print(array)
```

### Link do implementacji

{% embed url="https://ideone.com/ozVf3z" %}
Bubble sort - wersja zoptymalizowana
{% endembed %}

### Implementation descriptioni

W wersji zoptymalizowanej w każdym przebiegu głównej pętli (**linia 2**) sprawdzamy, czy podczas wykonania wewnętrznej pętli (**linia 5**) została dokonana jakaś zamiana elementów. W tym celu używamy dodatkowej zmiennej `swap`. Jeżeli żadna zamiana nie została wykonana (**linia 10**), to oznacza, że można zakończyć działanie algorytmu (**linia 11**), ponieważ lista została już posortowana.
