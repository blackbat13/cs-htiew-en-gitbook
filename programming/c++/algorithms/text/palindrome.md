# Palindrom

## Problem description

{% content-ref url="../../../../algorithms/text/palindrome.md" %}
[palindrome.md](../../../../algorithms/text/palindrome.md)
{% endcontent-ref %}

## Implementation

{% code overflow="wrap" lineNumbers="true" %}
```cpp
#include <iostream>
#include <algorithm>

using namespace std;

bool isPalindrome(string str) {
    string reversed = str;
    reverse(reversed.begin(), reversed.end());

    return str == reversed;
}

int main() {
    string str = "kajak";

    bool result = isPalindrome(str);

    if (result) {
        cout << str << " is a palindrome." << endl;
    } else {
        cout << str << " is not a palindrome." << endl;
    }

    return 0;
}
```
{% endcode %}

### Link do implementacji

{% embed url="https://ideone.com/UUUAe6" %}
Test palindromu
{% endembed %}
