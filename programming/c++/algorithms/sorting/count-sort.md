# Counting sort

## Problem description

{% content-ref url="../../../../algorithms/sorting/counting-sort.md" %}
[counting-sort.md](../../../../algorithms/sorting/counting-sort.md)
{% endcontent-ref %}

## Implementation

```cpp
#include <iostream>

using namespace std;

/// Sort ascending array of specified length
/// \param array - array to sort
/// \param n - length of the given array
void countingSort(int array[], int n) {
    int occurrences[100];
    int k = 0;
    for (int i = 0; i < 100; i++) {
        occurrences[i] = 0;
    }

    for (int i = 0; i < n; i++) {
        occurrences[array[i]]++;
    }

    for (int i = 0; i < 100; i++) {
        for (int j = 0; j < occurrences[i]; j++) {
            array[k] = i;
            k++;
        }
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
    
    countingSort(array, n);

    printArray(array, n);

    return 0;
}
```

### Link do implementacji

{% embed url="https://ideone.com/pUF5Jp" %}
Counting sort
{% endembed %}

### Implementation descriptioni

TODO
