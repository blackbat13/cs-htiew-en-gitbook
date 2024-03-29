# Naiwne wyszukiwanie wzorca w tekście

## Problem description

{% content-ref url="../../../../algorithms/text/naive-substring-search.md" %}
[naive-substring-search.md](../../../../algorithms/text/naive-substring-search.md)
{% endcontent-ref %}

## Implementation

{% code overflow="wrap" lineNumbers="true" %}
```cpp
#include <iostream>

using namespace std;

bool isSubstring(string a, string b) {
    int j;

    for (int i = 0; i < b.length() - a.length(); i++) {
        j = 0;
        while (j < a.length()) {
            if (a[j] == b[i + j]) {
                j++;
            } else {
                break;
            }
        }

        if (j == a.length()) {
            return true;
        }
    }

    return false;
}

int main() {
    string a = "kot";
    string b = "alamakota";

    bool result = isSubstring(a, b);

    if (result) {
        cout << a << " is substring of " << b << endl;
    } else {
        cout << a << " is not substring of " << b << endl;
    }

    return 0;
}
```
{% endcode %}

### Link do implementacji

{% embed url="https://ideone.com/S5zJSH" %}
Naiwne wyszukiwanie wzorca w tekście
{% endembed %}
