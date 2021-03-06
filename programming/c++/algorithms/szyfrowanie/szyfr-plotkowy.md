# Szyfr płotkowy

## Problem description

{% content-ref url="../../../../algorithms/algorytmy-szyfrowania/szyfr-plotkowy.md" %}
[szyfr-plotkowy.md](../../../../algorithms/algorytmy-szyfrowania/szyfr-plotkowy.md)
{% endcontent-ref %}

## Szyfrowanie

### Implementation

```cpp
#include <iostream>

using namespace std;

/// Encodes message using Rail Fence Cipher with given key
/// \param message - message to encode
/// \param key - key
/// \return message encode using Rail Fence with given key
string encode(string message, int key) {
    string encoded = "";
    int jump, i;

    for (int k = 0; k < key; k++) {
        if (k == key - 1) {
            jump = (key - 1) * 2;
        } else {
            jump = (key - (k + 1)) * 2;
        }
            
        i = k;
        
        while (i < message.length()) {
            encoded += message[i];
            i += jump;
        }
    }

    return encoded;
}

int main() {
    string message = "computer science";

    string encoded = encode(message, 3);

    cout << encoded << endl;
    
    return 0;
}
```

### Link do implementacji

{% embed url="https://ideone.com/8yVNZs" %}
Szyfrowanie szyfrem płotkowym
{% endembed %}

### Implementation descriptioni

TODO

## Deszyfrowanie

### Implementation

```cpp
#include <iostream>

using namespace std;

/// Decodes message using Rail Fence Cipher with given key
/// \param message - message to encode
/// \param key - key
/// \return message decoded using Rail Fence Cipher with given key
string decode(string message, int key) {
    string decoded = message;
    int j = 0;
    int jump, i;

    for (int k = 0; k < key; k++) {
        if (k == key - 1) {
            jump = (key - 1) * 2;
        } else {
            jump = (key - (k + 1)) * 2;
        }
        
        i = k;
        
        while (i < message.length()) {
            decoded[i] = message[j];
            j += 1;
            i += jump;
        }
    }
    
    return decoded;
}

int main() {
    string message = "cu eoptrsinemecc";

    string decoded = decode(message, 3);

    cout << decoded << endl;

    return 0;
}
```

### Link do implementacji

{% embed url="https://ideone.com/EA5DPk" %}
Deszyfrowanie szyfrem płotkowym
{% endembed %}

### Implementation descriptioni

TODO
