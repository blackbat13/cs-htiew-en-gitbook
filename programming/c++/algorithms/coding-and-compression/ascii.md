# ASCII codes

## Problem description

{% content-ref url="../../../../algorithms/coding-and-compression/ascii.md" %}
[ascii.md](../../../../algorithms/coding-and-compression/ascii.md)
{% endcontent-ref %}

## Podstawowa tablica ASCII

### Implementation

{% code overflow="wrap" lineNumbers="true" %}
```cpp
#include <iostream>

using namespace std;

int main() {
    char c;
    
    for (int i = 0; i <= 127; i++) {
        c = (char) i;
        cout << i << " = " << c << endl;
    }
    
    return 0;
}
```
{% endcode %}

### Link do implementacji

{% embed url="https://ideone.com/fnVCCi" %}
Podstawowa tablica ASCII
{% endembed %}

## Rozszerzona tablica ASCII

### Implementation

{% code overflow="wrap" lineNumbers="true" %}
```cpp
#include <iostream>

using namespace std;

int main() {
    unsigned char c;
    
    for (int i = 0; i <= 255; i++) {
        c = (unsigned char) i;
        cout << i << " = " << c << endl;
    }
    
    return 0;
}
```
{% endcode %}
