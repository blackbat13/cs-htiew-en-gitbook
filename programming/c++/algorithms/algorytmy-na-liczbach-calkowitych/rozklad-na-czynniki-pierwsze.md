# Rozkład na czynniki pierwsze

## Problem description

{% content-ref url="../../../../algorithms/algorytmy-na-liczbach-calkowitych/rozklad-na-czynniki-pierwsze.md" %}
[rozklad-na-czynniki-pierwsze.md](../../../../algorithms/algorytmy-na-liczbach-calkowitych/rozklad-na-czynniki-pierwsze.md)
{% endcontent-ref %}

## Implementation

```cpp
#include <iostream>

using namespace std;

/// Given integer n print its prime factors
/// \param n - number to check
void distribute(int n) {
    int i = 2;
    
    while(n > 1) {
        if(n % i == 0) {
            cout << i << " ";
            n /= i;
        } else {
            i++;
        }
    }
}

int main() {
    int n = 124;

    cout << "Prime factors of " << n << ": ";
    distribute(n);

    return 0;
}
```

### Link do implementacji

{% embed url="https://ideone.com/BiEykR" %}
Rozkład liczby na czynniki pierwsze
{% endembed %}

### Implementation descriptioni

TODO
