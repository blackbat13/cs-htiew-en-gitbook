# Prime factors

## Problem description

### Specification

#### Input

* $$n$$ - liczba naturalna, większa od zera

#### Output

* Rozkład liczby $$n$$ na czynniki pierwsze 

### Example

#### Input

```
n := 124
```

**Wynik**: $$2, 2, 31$$ 

## Solution

### Pseudocode

```
function PrimeFactors(n):
    1. i := 2
    2. While n > 1, do:
        3. If n mod i = 0, then:
            4. Print i
            5. n := n div i
        6. else:
            7. i := i + 1
```

{% hint style="info" %}
**mod** oznacza resztę z dzielenia

**div** oznacza dzielenie całkowite
{% endhint %}

### Block diagram

```mermaid
flowchart TD
	START(["PrimeFactors(n)"]) --> K1[i := 2]
	K1 --> K2{n > 1}
	K2 -- TRUE --> K3{n mod i = 0}
	K3 -- TRUE --> K4[/Print i/]
	K4 --> K5[n := n div i]
	K5 --> K2
	K3 -- FALSE --> K7[i := i + 1]
	K7 --> K2
	K2 -- FALSE ----> STOP([STOP])
```

## Implementation

### C++

{% content-ref url="../../programming/c++/algorithms/integers/prime-factors.md" %}
[prime-factors.md](../../programming/c++/algorithms/integers/prime-factors.md)
{% endcontent-ref %}

### Python

{% content-ref url="../../programming/python/algorithms/integers/prime-factors.md" %}
[prime-factors.md](../../programming/python/algorithms/integers/prime-factors.md)
{% endcontent-ref %}
