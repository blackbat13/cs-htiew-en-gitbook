# Suma dwóch liczb

## Problem description

{% content-ref url="../../../../algorithms/searching/sum-of-two.md" %}
[sum-of-two.md](../../../../algorithms/searching/sum-of-two.md)
{% endcontent-ref %}

## Naive solution

### Implementation

{% code overflow="wrap" lineNumbers="true" %}
```cpp
#include <iostream>

using namespace std;

void sumOfTwoNaive(int n, int tab[], int sum) {
    for (int i = 0; i < n; i++) {
        for (int j = i+1; j < n; j++) {
            if (tab[i] + tab[j] == sum) {
                cout << tab[i] << ", " << tab[j] << endl;
                return;
            }
        }
    }
    
    cout << -1 << endl;
}

int main() {
    int n = 10;
    int tab[10] = {1, 2, 4, 6, 8, 9, 10, 12, 13, 15};
    int sum = 18;

    sumOfTwoNaive(n, tab, sum);

    return 0;
}
```
{% endcode %}

### Link do implementacji

{% embed url="https://ideone.com/dHf2jV" %}
Suma dwóch - rozwiązanie naiwne
{% endembed %}

## Optimal solution

### Implementation

{% code overflow="wrap" lineNumbers="true" %}
```cpp
#include <iostream>

using namespace std;

void sumOfTwoOptimal(int n, int tab[], int sum) {
    int left = 0;
    int right = n-1;

    while (left < right && tab[left] + tab[right] != sum) {
        if (tab[left] + tab[right] < sum) {
            left++;
        } else {
            right--;
        }
    }

    if (left < right) {
        cout << tab[left] << ", " << tab[right] << endl;
    } else {
        cout << -1 << endl;
    }
}

int main() {
    int n = 10;
    int tab[10] = {1, 2, 4, 6, 8, 9, 10, 12, 13, 15};
    int sum = 18;

    sumOfTwoOptimal(n, tab, sum);
    
    return 0;
}
```
{% endcode %}

### Link do implementacji

{% embed url="https://ideone.com/QuNr8P" %}
Suma dwóch - rozwiązanie optymalne
{% endembed %}
