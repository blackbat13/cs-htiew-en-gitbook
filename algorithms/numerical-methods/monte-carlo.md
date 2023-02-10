# Monte Carlo method

## Problem description

## Obliczanie przybliżonej wartości liczby PI

### Specification

#### Input

* $$n$$ — liczba prób (im większa, tym większa dokładność)

#### Output

* $$pi$$ — przybliżona wartość liczby $$\pi$$

### Solution

### Pseudocode

```
function MonteCarloPI(n)
    1. inside := 0
    2. From i := 1 to n, do:
        3. x := random real number from -1 to 1
        4. y := random real number from -1 to 1
        5. dist := (x * x) + (y * y)
        6. If dist <= 1, then:
            7. inside := inside + 1
    
    8. Return ((4 * inside) / n)
```

### Block diagram

```mermaid
flowchart TD
	START(["MonteCarloPi(n)"]) --> K1[inside := 0\ni := 1]
	K1 --> K2{i <= n}
	K2 -- TRUE --> K3["x := random(-1, 1)\ny := random(-1, 1)\ndist := x * x + y * y"]
	K3 --> K6{dist <= 1}
	K6 -- TRUE --> K7[inside := inside + 1]
	K7 --> K2i[i := i + 1]
	K6 -- FALSE --> K2i
	K2i --> K2
	K2 -- FALSE ---> K8[/"Return ((4 * inside) / n)"/]
	K8 ---> STOP([STOP])
```

## Implementation

### C++

{% content-ref url="../../programming/c++/algorithms/numerical-methods/monte-carlo.md" %}
[monte-carlo.md](../../programming/c++/algorithms/numerical-methods/monte-carlo.md)
{% endcontent-ref %}

### Python

{% content-ref url="../../programming/python/algorithms/numerical-methods/monte-carlo.md" %}
[monte-carlo.md](../../programming/python/algorithms/numerical-methods/monte-carlo.md)
{% endcontent-ref %}
