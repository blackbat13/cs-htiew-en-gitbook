---
description: Największy Wspólny Dzielnik
---

# GCD

## Problem description

{% content-ref url="../../../../algorithms/integers/gcd.md" %}
[gcd.md](../../../../algorithms/integers/gcd.md)
{% endcontent-ref %}

## Wersja z odejmowaniem

### Implementation

{% code overflow="wrap" lineNumbers="true" %}
```cpp
#include <iostream>

using namespace std;

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
    int a = 32;
    int b = 12;
    
    int result = gcd(a, b);

    cout << "gcd(" << a << "," << b << ") = " << result << endl;

    return 0;
}
```
{% endcode %}

### Link do implementacji

{% embed url="https://ideone.com/GkELPX" %}
Obliczanie NWD za pomocą algorytmu z odejmowaniem
{% endembed %}

## Iterative GCD with modulo

### Implementation

{% code overflow="wrap" lineNumbers="true" %}
```cpp
#include <iostream>

using namespace std;

int gcd(int a, int b) {
    while(b != 0) {
        int b2 = b;
        b = a % b;
        a = b2;
    }

    return a;
}

int main() {
    int a = 32;
    int b = 12;
    
    int result = gcd(a, b);

    cout << "gcd(" << a << "," << b << ") = " << result << endl;

    return 0;
}
```
{% endcode %}

### Link do implementacji

{% embed url="https://ideone.com/qHVLNg" %}
Obliczanie NWD za pomocą iteracyjnego algorytmu Euklidesa
{% endembed %}

## Recursive GCD with modulo

### Implementation

```cpp
#include <iostream>

using namespace std;

int gcd(int a, int b) {
    if(b == 0) {
        return a;
    }

    return gcd(b, a % b);
}

int main() {
    int a = 32;
    int b = 12;
    
    int result = gcd(a, b);

    cout << "gcd(" << a << "," << b << ") = " << result << endl;

    return 0;
}
```
{% endcode %}

### Link do implementacji

{% embed url="https://ideone.com/TNVI7N" %}
Obliczanie NWD za pomocą rekurencyjnego algorytmu Euklidesa
{% endembed %}

## Operacje binarne - wersja iteracyjna

### Implementation

```cpp
#include <iostream>

using namespace std;

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
    int a = 32;
    int b = 12;
    
    int result = gcd(a, b);

    cout << "gcd(" << a << "," << b << ") = " << result << endl;

    return 0;
}
```
{% endcode %}

### Link do implementacji

{% embed url="https://ideone.com/eL2zBM" %}
Binarne NWD - wersja iteracyjna
{% endembed %}

## Operacje binarne - wersja rekurencyjna

### Implementation

{% code overflow="wrap" lineNumbers="true" %}
```cpp
#include <iostream>

using namespace std;

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
    int a = 32;
    int b = 12;
    
    int result = gcd(a, b);

    cout << "gcd(" << a << "," << b << ") = " << result << endl;
    return 0;
}
```
{% endcode %}

### Link do implementacji

{% embed url="https://ideone.com/ujhy7u" %}
Binarne NWD - wersja rekurencyjna
{% endembed %}
