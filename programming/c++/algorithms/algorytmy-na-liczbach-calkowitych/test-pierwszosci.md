# Test pierwszości

## Problem description

{% content-ref url="../../../../algorithms/algorytmy-na-liczbach-calkowitych/test-pierwszosci.md" %}
[test-pierwszosci.md](../../../../algorithms/algorytmy-na-liczbach-calkowitych/test-pierwszosci.md)
{% endcontent-ref %}

## Implementation

```cpp
#include <iostream>
#include <cmath>

using namespace std;

/// Check if n is prime
/// \param n - number to check
/// \return true if n is a prime number, false otherwise
bool isPrime(int n) {
    if (n < 2) {
        return false;
    }

    for (int i = 2; i <= sqrt(n); i++) {
        if(n % i == 0) {
            return false;
        }
    }

    return true;
}

int main() {
    int n = 7;
    
    if (isPrime(n)) {
        cout << n << " is prime" << endl;
    } else {
        cout << n << " is not prime" << endl;
    }

    return 0;
}
```

### Link do implementacji

{% embed url="https://ideone.com/0vg44U" %}
Test pierwszości
{% endembed %}

### Implementation descriptioni

TODO
