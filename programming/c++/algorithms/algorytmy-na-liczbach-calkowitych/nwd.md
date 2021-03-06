---
description: Największy Wspólny Dzielnik
---

# NWD

## Problem description

{% content-ref url="../../../../algorithms/algorytmy-na-liczbach-calkowitych/algorytm-euklidesa.md" %}
[algorytm-euklidesa.md](../../../../algorithms/algorytmy-na-liczbach-calkowitych/algorytm-euklidesa.md)
{% endcontent-ref %}

## Wersja z odejmowaniem

### Implementation

```cpp
#include <iostream>

using namespace std;

/// Counts gcd(a,b) using subtraction method
/// \return gcd(a,b)
int gcd(int a, int b) {
    while (a != b) {
        if (a > b) {
            a -= b;
        } else {
            b -= a;
        }
    }

    return a;
}

int main() {
    int a, b, result;
    
    a = 32;
    b = 12;
    
    result = gcd(a, b);

    cout << "gcd(" << a << "," << b << ") = " << result << endl;
    return 0;
}
```

### Link do implementacji

{% embed url="https://ideone.com/GkELPX" %}
Obliczanie NWD za pomocą algorytmu z odejmowaniem
{% endembed %}

### Implementation descriptioni

TODO

## Algorytm Euklidesa - wersja iteracyjna

### Implementation

```cpp
#include <iostream>

using namespace std;

/// Counts gcd(a,b) using Euklides iterative algorithm
/// \return gcd(a,b)
int gcd(int a, int b) {
    while(b != 0) {
        int b2 = b;
        b = a%b;
        a = b2;
    }

    return a;
}

int main() {
    int a, b, result;
    
    a = 32;
    b = 12;
    
    result = gcd(a, b);

    cout << "gcd(" << a << "," << b << ") = " << result << endl;
    return 0;
}
```

### Link do implementacji

{% embed url="https://ideone.com/qHVLNg" %}
Obliczanie NWD za pomocą iteracyjnego algorytmu Euklidesa
{% endembed %}

### Implementation descriptioni

TODO

## Algorytm Euklidesa - wersja rekurencyjna

### Implementation

```cpp
#include <iostream>

using namespace std;

/// Counts gcd(a,b) using Euklides recursive algorithm
/// \return gcd(a,b)
int gcd(int a, int b) {
    if(b == 0) {
        return a;
    }

    return gcd(b, a%b);
}

int main() {
    int a, b, result;
    
    a = 32;
    b = 12;
    
    result = gcd(a, b);

    cout << "gcd(" << a << "," << b << ") = " << result << endl;
    return 0;
}
```

### Link do implementacji

{% embed url="https://ideone.com/TNVI7N" %}
Obliczanie NWD za pomocą rekurencyjnego algorytmu Euklidesa
{% endembed %}

### Implementation descriptioni

TODO

## Operacje binarne - wersja iteracyjna

### Implementation

```cpp
#include <iostream>

using namespace std;

/// Computes gcd(a,b) using iterative method
/// \return gcd(a,b)
int gcd(int a, int b) {
    int shift;

    if (a == 0) {
        return b;
    }

    if (b == 0) {
        return a;
    }

    for (shift = 0; ((a | b) & 1) == 0; shift++) {
        a >>= 1;
        b >>= 1;
    }

    while ((a & 1) == 0) {
        a >>= 1;
    }

    while (b != 0) {
        while ((b & 1) == 0) {
            b >>= 1;
        }

        if (a > b) {
            swap(a, b);
        }

        b = b - a;
    }

    return a << shift;
}

int main() {
    int a, b, result;
    
    a = 32;
    b = 12;
    
    result = gcd(a, b);

    cout << "gcd(" << a << "," << b << ") = " << result << endl;
    return 0;
}
```

### Link do implementacji

{% embed url="https://ideone.com/eL2zBM" %}
Binarne NWD - wersja iteracyjna
{% endembed %}

### Implementation descriptioni

TODO

## Operacje binarne - wersja rekurencyjna

### Implementation

```cpp
#include <iostream>

using namespace std;

/// Computes gcd(a,b) using recursive method
/// \return gcd(a,b)
int gcd(int a, int b) {
    if (a == b) {
        return a;
    }

    if (a == 0) {
        return b;
    }

    if (b == 0) {
        return a;
    }

    if (~a & 1) {
        if (b & 1) {
            return gcd(a >> 1, b);
        } else {
            return gcd(a >> 1, b >> 1) << 1;
        }
    }

    if (~b & 1) {
        return gcd(a, b >> 1);
    }

    if (a > b) {
        return gcd((a - b) >> 1, b);
    }

    return gcd((b - a) >> 1, a);
}

int main() {
    int a, b, result;
    
    a = 32;
    b = 12;
    
    result = gcd(a, b);

    cout << "gcd(" << a << "," << b << ") = " << result << endl;
    return 0;
}
```

### Link do implementacji

{% embed url="https://ideone.com/ujhy7u" %}
Binarne NWD - wersja rekurencyjna
{% endembed %}

### Implementation descriptioni

TODO
