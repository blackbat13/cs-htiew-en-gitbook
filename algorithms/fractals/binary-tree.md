# Drzewo binarne

## Opis problemu

TODO

### Specyfikacja

#### Dane

* $$n$$ - stopień drzewa binarnego
* $$w$$ - początkowa długość gałęzi (pnia)

#### Wynik

* Drzewo binarne stopnia $$n$$ i początkowej długości $$w$$.

### Prezentacja

{% file src="../../.gitbook/assets/Drzewo Binarne (1).pdf" %}
Drzewo binarne - wprowadzenie
{% endfile %}

## Rozwiązanie

### Prezentacja

{% file src="../../.gitbook/assets/Drzewo Binarne - algorytm (1).pdf" %}
Drzewo binarne - algorytm
{% endfile %}

### Pseudokod

```
function BinaryTree(n, w):
    1. Forward(w)
    2. If n > 0, then:
        3. Left(45)
        4. BinaryTree(n - 1, w / 2)
        5. Right(90)
        6. BinaryTree(n - 1, w / 2)
        7. Left(45)
    8. Back(w)
```

### Block diagram

```mermaid
flowchart TD
	START(["BinaryTree(n, w)"]) --> K1["Forward(w)"]
	K1 --> K2{n > 0}
	K2 -- TRUE --> K3["Left(45)\nBinaryTree(n - 1, w / 2)\nRight(90)\nBinaryTree(n - 1, w / 2)\nLeft(45)"]
	K3 --> K8["Back(w)"]
	K2 -- FALSE --> K8
	K8 --> STOP([STOP])
```

## Implementacja

### C++

{% content-ref url="../../programming/c++/algorithms/fractals/binary-tree.md" %}
[binary-tree.md](../../programming/c++/algorithms/fractals/binary-tree.md)
{% endcontent-ref %}

### Python

{% content-ref url="../../programming/python/algorithms/fractals/binary-tree.md" %}
[binary-tree.md](../../programming/python/algorithms/fractals/binary-tree.md)
{% endcontent-ref %}

### Blockly

{% content-ref url="../../programming/blockly/algorithms/fractals/binary-tree.md" %}
[binary-tree.md](../../programming/blockly/algorithms/fractals/binary-tree.md)
{% endcontent-ref %}
