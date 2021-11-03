# Drzewo binarne

## Problem description

TODO

### Specification

#### Input

* $$n$$ - stopień drzewa binarnego
* $$w$$ - początkowa długość gałęzi (pnia)

#### Output

* Drzewo binarne stopnia $$n$$ i początkowej długości $$w$$.

### Prezentacja

{% file src="../../.gitbook/assets/Drzewo Binarne (1).pdf" %}
Drzewo binarne - wprowadzenie
{% endfile %}

## Solution

### Prezentacja

{% file src="../../.gitbook/assets/Drzewo Binarne - algorytm (1).pdf" %}
Drzewo binarne - algorytm
{% endfile %}

### Pseudocode

```
funkcja DrzewoBinarne(n, w):
    1. Idź do przodu o w
    2. Jeżeli n > 0, to:
        3. Obróć się w lewo
        4. Wywołaj DrzewoBinarne(n - 1, w / 2)
        5. Obróć się w prawo
        6. Wywołaj DrzewoBinarne(n - 1, w / 2)
        7. Obróć się w lewo (do początkowego ustawienia)
    8. Idź do tyłu o w
```

## Implementation

### Python

{% content-ref url="../../programming/python/algorithms/fraktale/drzewo-binarne.md" %}
[drzewo-binarne.md](../../programming/python/algorithms/fraktale/drzewo-binarne.md)
{% endcontent-ref %}

### Blockly

{% content-ref url="../../programming/blockly/algorithms/fraktale-1/drzewo-binarne.md" %}
[drzewo-binarne.md](../../programming/blockly/algorithms/fraktale-1/drzewo-binarne.md)
{% endcontent-ref %}
