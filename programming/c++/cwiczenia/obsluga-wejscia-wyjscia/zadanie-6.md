# Zadanie 6

## Treść zadania

Napisz program zgodny z poniższą specyfikacją. Wykorzystaj funkcję **min**.

### Specyfikacja

#### Input

* $$a, b$$ - dwie liczby całkowite

#### Wynik

* Mniejsza z liczb $$a$$ i $$b$$, lub dowolna gdy są sobie równe

## Solution

```cpp
#include <iostream>

using namespace std;

int main() {
    int a, b, wynik;
    
    cout << "Podaj dwie liczby:" << endl;
    cin >> a >> b;
    
    wynik = min(a, b);
    
    cout << "Minimum: " << wynik << endl;
    
    return 0;
}
```
