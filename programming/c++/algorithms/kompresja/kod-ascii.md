# Kod ASCII

## Problem description

{% content-ref url="../../../../algorithms/kompresja/kod-ascii.md" %}
[kod-ascii.md](../../../../algorithms/kompresja/kod-ascii.md)
{% endcontent-ref %}

## Podstawowa tablica ASCII

### Implementation

```cpp
#include <iostream>
using namespace std;

int main() {
    char c;
    
    for(int i = 0; i <= 127; i++) {
        c = (char)i;
        cout << i << " = " << c << endl;
    }
    
    return 0;
}
```

### Link do implementacji

{% embed url="https://ideone.com/fnVCCi" %}
Podstawowa tablica ASCII
{% endembed %}

### Implementation descriptioni

TODO

## Rozszerzona tablica ASCII

### Implementation

```cpp
#include <iostream>
using namespace std;

int main() {
    unsigned char c;
    
    for(int i = 0; i <= 255; i++) {
        c = (unsigned char)i;
        cout << i << " = " << c << endl;
    }
    
    return 0;
}
```

### Implementation descriptioni

TODO
