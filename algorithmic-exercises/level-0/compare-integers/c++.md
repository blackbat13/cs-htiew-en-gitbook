# C++

```cpp
#include <iostream>

using namespace std;

int main() {
    int a, b;
    
    cout << "Podaj a:" << endl;
    cin >> a;
    
    cout << "Podaj b:" << endl;
    cin >> b;
    
    if (a == b) {
        cout << "=" << endl;
    } else if (a < b) {
        cout << "<" << endl;
    } else {
        cout << ">" << endl;
    }

    return 0;
}
```

## Implementation description

At the beginning we declare two integer variables `a` and `b` for the storage of the input data (**line 5**). Then we load two values ​​from the user (**lines 7-11**), providing the messages used.

Then, using the conditional instructions, we check the relationship between loaded values. If the variable values ​​`a` and `b` are equal (**line 13**), we write an equal sign (**line 14**). Otherwise, if the value of the variable `a` is lower than the variable value `b` (**line 15**), then we write a minority sign (**line 16**). Otherwise (**line 17**) we write the sign of the majority (**line 18**).

Note that in the last part of the conditional instructions (**line 17**), we no longer need to check whether the value of the variable `a` is greater than the value of the variable `b`. This is due to previous conditions. If the variable values ​​are not equal to each other or `a` is not smaller than `b`, we know that `a` is greater than `b`.



