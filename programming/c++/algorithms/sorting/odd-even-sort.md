# Odd-Even sort

## Opis problemu

{% content-ref url="../../../../algorithms/sorting/odd-even-sort.md" %}
[odd-even-sort.md](../../../../algorithms/sorting/odd-even-sort.md)
{% endcontent-ref %}

## Implementation

```cpp
#include <iostream>

using namespace std;

/// Sorts the array in ascending order
/// \param array - array to sort
/// \param length - length of given array
void oddEvenSort(int array[], int n) {
    for (int i = 0; i < n; i++) {
        if (i % 2 == 1) {
            for (int j = 2; j < n; j += 2) {
                if (array[j] < array[j - 1]) {
                    swap(array[j], array[j - 1]);
                }
            }
        } else {
            for (int j = 1; j < n; j += 2) {
                if (array[j] < array[j - 1]) {
                    swap(array[j], array[j - 1]);
                }
            }
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
    
    oddEvenSort(array, n);
    
    printArray(array, n);

    return 0;
}
```

### Link do implementacji

{% embed url="https://ideone.com/8K0kEO" %}
Odd-Even sort
{% endembed %}

### Opis implementacji

TODO
