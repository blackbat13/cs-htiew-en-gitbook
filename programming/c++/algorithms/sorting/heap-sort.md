# Heap sort

## Opis problemu

{% content-ref url="../../../../algorithms/sorting/heap-sort.md" %}
[heap-sort.md](../../../../algorithms/sorting/heap-sort.md)
{% endcontent-ref %}

## Implementation

```cpp
#include <iostream>

using namespace std;

void buildHeap(int array[], int n) {
    for (int i = 1; i < n; i++) {
        int parentIndex = (i - 1) / 2;
        int j = i;
        while (j > 0 && array[j] > array[parentIndex]) {
            swap(array[j], array[parentIndex]);
            j = parent_index;
            parentIndex = (j - 1) / 2;
        }
    }
}

void heapSort(int array[], int n) {
    for (int i = n - 1; i > 0; i--) {
        buildHeap(array, i + 1);
        swap(array[0], array[i]);
    }
}

/// Prints given array
/// \param array - array to print
/// \param n - length of the given array
void printArray(int array[], int n) {
    for(int i = 0; i < 10; ++i) {
        cout << array[i] << " ";
    }
 
    cout << endl;
}

int main() {
    int array[10] = {7, 3, 0, 1, 5, 2, 5, 19, 10, 5};
    int n = 10;
    
    heapSort(array, n);

    printArray(array, n);

    return 0;
}
```

### Link do implementacji

{% embed url="https://ideone.com/D8K2zO" %}
Heap sort
{% endembed %}

### Opis implementacji

TODO
