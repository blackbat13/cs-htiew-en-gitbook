# Introduction

Programming is an art. The programmer is like an artist who takes a blank canvas and leaves a masterpiece on it.

Before we start the adventure with programming, let's take a look at the available "tools", ie **programming languages**. Of course, we won't cover all of them, it wouldn't make much sense. We will focus on some classics.

We will compare different languages by looking at the implementation of a simple program: a **coin toss simulator**. We will not focus here on a detailed discussion of the implementation and individual instructions. The goal is to look at different languages from a bird's eye view.

The idea behind the program is simple. At the beginning we draw an integer: **0** or **1**, this is to simulate our coin toss. Then, depending on the drawn value, we write an appropriate message to the screen. If we have drawn **0**, it means **Heads **is the result. Otherwise (i.e. when we drew **1**), **Tails **was the result.

We encourage you to test the following programs. Under each implementation, there is a link to that implementation on the _Ideone _website. There you can run a given program, which is best done several times to see what values (**Heads **or **Tails**) will be printed on the screen.

## Python 3

```python
import random

coin = random.randint(0, 1)

if coin == 0:
    print("Heads")
else:
    print("Tails")
```

{% embed url="https://ideone.com/uMTxg9" %}
Symulator rzutu monetą - Python
{% endembed %}

## C++

```cpp
#include <iostream>
#include <ctime>
#include <random>
using namespace std;

int main() {
    srand(time(NULL));
    
    int coin;
    coin = rand() % 2;
    
    if(coin == 0) {
        cout << "Head" << endl;
    } else {
        cout << "Tails" << endl;
    }
    
    return 0;
}
```

{% embed url="https://ideone.com/ewTF4L" %}
Symulator rzutu monetą - C++
{% endembed %}

## Java

```java
import java.util.*;
import java.lang.*;
import java.io.*;

class Main {
    public static void main (String[] args) throws java.lang.Exception {
        Random rd = new Random(); 
        
        int coin = rd.nextInt(2);
        
        if(coin == 0) {
            System.out.println("Heads");
        } else {
            System.out.println("Tails");
        }
    }
}
```

{% embed url="https://ideone.com/gLqkST" %}
Symulator rzutu monetą - Java
{% endembed %}

## Pascal

```pascal
program cointoss;
	var coin : integer;
begin
	randomize();
	
	coin := random(2);
	
	if coin = 0 then write('Heads')
	else write ('Tails')
end.
```

{% embed url="https://ideone.com/w7bHvU" %}
Symulator rzutu monetą - Pascal
{% endembed %}

## Blockly

![Symulator rzutu monetą](<../.gitbook/assets/image (8).png>)

{% embed url="https://blockly-demo.appspot.com/static/demos/code/index.html?lang=pl#gsq3of" %}
Symulator rzutu monetą - Blockly
{% endembed %}
