# Fast exponentiation

## Problem description

{% content-ref url="../../../../algorithms/numerical-methods/fast-exp.md" %}
[fast-exp.md](../../../../algorithms/numerical-methods/fast-exp.md)
{% endcontent-ref %}

## Iterative solution

{% code overflow="wrap" lineNumbers="true" %}
```cpp
#include <iostream>

using namespace std;

int fastExp(int a, int n) {
    int result = 1;

    while (n > 0) {
        if (n % 2 == 1) {
            result *= a;
        }

        a *= a;
        n /= 2;
    }

    return result;
}

int main() {
    int a = 2;
    int n = 10;

    int result = fastExp(a, n);
    
    cout << a << "^" << n << " = " << result << endl;
    
    return 0;
}
```
{% endcode %}

### Link do implementacji

{% embed url="https://ideone.com/pdUCOO" %}
Szybkie potęgowanie - wersja iteracyjna
{% endembed %}

## Recursive solution

{% code overflow="wrap" lineNumbers="true" %}
```cpp
#include <iostream>

using namespace std;

int fastExp(int a, int n) {
    if (n == 0) {
        return 1;
    }

    int result = fastExp(a, n / 2);

    if (n % 2 == 1) {
        return result * result * a;
    } else {
        return result * result;
    }
}

int main() {
    int a = 2;
    int n = 10;

    int result = fastExp(a, n);
    
    cout << a << "^" << n << " = " << result << endl;
    
    return 0;
}
```
{% endcode %}

### Link do implementacji

{% embed url="https://ideone.com/zE3iXb" %}
Szybkie potęgowanie - wersja rekurencyjna
{% endembed %}