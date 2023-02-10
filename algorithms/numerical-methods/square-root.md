# Square root

## Problem description

Jak policzyć pierwiastek kwadratowy z podanej liczby, gdy nie mamy przy sobie kalkulatora, ani wbudowanych metod programistycznych?

### Specification

#### Input

* $$n$$ — liczba rzeczywista.
* $$p$$ — liczba rzeczywista, dokładność.

#### Output

* $$\sqrt{n}$$ policzony z dokładnością $$p$$

## Solution — metoda Herona

### Pseudocode

```
function HeronMethod(n, p):
    1. x1 := n / 2
    2. x2 := (x1 + (n / x1)) / 2
    3. While |x2 - x1| > p, do:
        4. x1 := (x2 + (n / x2)) / 2
        5. Swap(x1, x2)
    6. Return x2
```

### Block diagram

```mermaid
flowchart TD
	START(["HeronMethod(n, p)"]) --> K1["x1 := n / 2\nx2 := (x1 + (n / x1)) / 2"]
	K1 --> K3{"|x2 - x1| > p"}
	K3 -- TRUE --> K4["x1 := (x2 + (n / x2)) / 2\nSwap(x1, x2)"]
	K4 --> K3
    K3 -- FALSE --> K6[/Return x2/]
    K6 --> STOP([STOP])
```

## Implementation

### C++

{% content-ref url="../../programming/c++/algorithms/numerical-methods/square-root.md" %}
[square-root.md](../../programming/c++/algorithms/numerical-methods/square-root.md)
{% endcontent-ref %}

### Python

{% content-ref url="../../programming/python/algorithms/numerical-methods/square-root.md" %}
[square-root.md](../../programming/python/algorithms/numerical-methods/square-root.md)
{% endcontent-ref %}
