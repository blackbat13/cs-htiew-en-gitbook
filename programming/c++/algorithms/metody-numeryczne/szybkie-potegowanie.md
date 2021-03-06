# Szybkie potęgowanie

## Problem description

{% content-ref url="../../../../algorithms/metody-numeryczne/szybkie-potegowanie.md" %}
[szybkie-potegowanie.md](../../../../algorithms/metody-numeryczne/szybkie-potegowanie.md)
{% endcontent-ref %}

## Implementation

```cpp
#include <iostream>

using namespace std;

/// Count a^n using the binary representation of n
/// \param a - number to rise
/// \param n - power
/// \return a^n
int fastExp(int a, int n) {
    int w = 1;

    while (n > 0) {
        if (n % 2 == 1) {
            w *= a;
        }

        a *= a;
        n /= 2;
    }

    return w;
}

int main() {
    int a = 2;
    int n = 10;
    int result = fastExp(a, n);
    
    cout << a << "^" << n << " = " << result << endl;
    
    return 0;
}
```

### Link do implementacji

{% embed url="https://ideone.com/pdUCOO" %}
Szybkie potęgowanie
{% endembed %}

### Implementation descriptioni

TODO
