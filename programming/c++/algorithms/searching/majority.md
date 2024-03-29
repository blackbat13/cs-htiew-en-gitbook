# Znajdowanie lidera w zbiorze

## Problem description

{% content-ref url="../../../../algorithms/searching/majority.md" %}
[majority.md](../../../../algorithms/searching/majority.md)
{% endcontent-ref %}

## Implementation

{% code overflow="wrap" lineNumbers="true" %}
```cpp
#include <iostream>

using namespace std;

int countOccurences(int number, int array[], int length) {
    int result = 0;

    for (int i = 0; i < length; i++) {
        if (array[i] == number) {
            result++;
        }
    }

    return result;
}

int findLeader(int array[], int length) {
    int counter = 1;
    int currentCandidate = array[0];
    
    for (int i = 1; i < length; i++) {
        if (counter == 0) {
            currentCandidate = array[i];
            counter = 1;
        } else if (array[i] == currentCandidate) {
            counter++;
        } else {
            counter--;
        }
    }

    counter = countOccurences(currentCandidate, array, length);

    if (counter > length / 2) {
        return currentCandidate;
    } else {
        return -1;
    }
}

int main() {
    int array[10] = {1, 2, 5, 5, 7, 5, 5, 10, 5, 5};

    int majority = findLeader(array, 10);

    cout << majority << endl;

    return 0;
}
```
{% endcode %}

### Link do implementacji

{% embed url="https://ideone.com/oeuyQq" %}
Znajdowanie lidera w zbiorze
{% endembed %}
