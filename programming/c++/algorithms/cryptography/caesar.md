# Caesar cipher

## Problem description

{% content-ref url="../../../../algorithms/cryptography/caesar.md" %}
[caesar.md](../../../../algorithms/cryptography/caesar.md)
{% endcontent-ref %}

## Encoding

### Implementation

{% code overflow="wrap" lineNumbers="true" %}
```cpp
#include <iostream>

using namespace std;

string encryptCaesar(string message, int key) {
    string result = "";
    char encrypted;
    
    key %= 26;
    
    for(char letter : message) {
        encrypted = letter + key;
        if(encrypted > 'z') {
            encrypted = encrypted - 'z' + 'a' - 1;
        }
        
        result += encrypted;
    }
    
    return result;
}

int main() {
    string message = "alamakota";
    int key = 3;
    
    string encrypted = encryptCaesar(message, key);
    
    cout << encrypted << endl;
    
    return 0;
}
```
{% endcode %}

### Link do implementacji

{% embed url="https://ideone.com/nX9kLA" %}
Szyfrowanie Cezara
{% endembed %}

## Decoding

### Implementation

{% code overflow="wrap" lineNumbers="true" %}
```cpp
#include <iostream>

using namespace std;

string decryptCaesar(string encrypted, int key) {
    string result = "";
    char decrypted;
    
    key %= 26;
    
    for(char letter : encrypted) {
        decrypted = letter - key;
        if(decrypted < 'a') {
            decrypted = 'z' - ('a' - decrypted - 1);
        }
        
        result += decrypted;
    }
    
    return result;
}

int main() {
    string encrypted = "dodpdnrwd";
    int key = 3;
    
    string decrypted = decryptCaesar(encrypted, key);
    
    cout << decrypted << endl;
    
    return 0;
}
```
{% endcode %}

### Link do implementacji

{% embed url="https://ideone.com/641y0x" %}
Deszyfrowanie Cezara
{% endembed %}
