# Odległość Hamminga

## Problem description

{% content-ref url="../../../../algorithms/tekstowe/odleglosc-hamminga.md" %}
[odleglosc-hamminga.md](../../../../algorithms/tekstowe/odleglosc-hamminga.md)
{% endcontent-ref %}

## Implementation

```cpp
#include <iostream>

using namespace std;

/// Computes Hamming distance between the two words of equal length
/// \param a - first word
/// \param b - second word
/// \return Hamming distance between a and b
int hammingDistance(string a, string b) {
    int distance = 0;
    
    for (int i = 0; i < a.length(); i++) {
        if (a[i] != b[i]) {
            distance++;
        }
    }

    return distance;
}

int main() {
    string a, b;
    int distance;
    
    a = "karolin";
    b = "kerstin";
    
    distance = hammingDistance(a, b);
    
    cout << "Hamming distance between words " << a << " and " << b << " is " << distance << endl;
    return 0;
}
```

### Link do implementacji

{% embed url="https://ideone.com/OVl4FY" %}
Odległość Hamminga
{% endembed %}

### Implementation descriptioni

TODO
