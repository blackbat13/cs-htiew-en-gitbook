# Sortowanie bąbelkowe

## Problem description

{% content-ref url="../../../../algorithms/sorting/bubble-sort.md" %}
[bubble-sort.md](../../../../algorithms/sorting/bubble-sort.md)
{% endcontent-ref %}

## Implementation

{% code overflow="wrap" lineNumbers="true" %}
```cpp
#include <iostream>

using namespace std;

void bubbleSort(int array[], int n) {
	bool sorted = false;
	int i = 0;
    while (!sorted) {
    	sorted = true;
        for(int j = n - 1; j > i; j--) {
            if(array[j] < array[j-1]) {
                swap(array[j], array[j-1]);
                sorted = false;
            }
        }
        
        i++;
    }
}

void printArray(int array[], int n) {
    for(int i = 0; i < 10; ++i) {
        cout << array[i] << " ";
    }
 
    cout << endl;
}

int main() {
    int array[10] = {7, 3, 0, 1, 5, 2, 5, 19, 10, 5};
    int n = 10;
    
    bubbleSort(array, n);

    printArray(array, n);

    return 0;
}
```
{% endcode %}

### Link do implementacji

{% embed url="https://ideone.com/rnfrjy" %}
Sortowanie bąbelkowe
{% endembed %}