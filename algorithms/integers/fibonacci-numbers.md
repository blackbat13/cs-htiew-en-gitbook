# Fibonacci numbers

## Problem description

TODO

### Specification

#### Input

* $$n$$ - liczba naturalna, większa od zera

#### Output

* $$n$$-ta liczba Fibonacciego

### Example

#### Input

```
n := 10
```

**Wynik**: $$55$$ 

{% hint style="info" %}
**Wyjaśnienie**

Pierwszych kolejnych dziesięć liczb Fibonacciego to: $$1, 1, 2, 3, 5, 8, 13, 21, 34, 55$$ 
{% endhint %}

## Recursive solution

### Pseudocode

```
function Fib(n):
    1. If n <= 2, then:
        2. Return 1
    3. Return Fib(n - 1) + Fib(n - 2)
```

### Block diagram

```mermaid
flowchart TD
	START(["Fib(n)"]) --> K1{n <= 2}
	K1 -- TRUE --> K2[/Return 1/]
	K2 --> STOP([STOP])
	K1 -- FALSE --> K3[/"Return Fib(n - 1) + Fib(n - 2)"/]
	K3 --> STOP
```

## Iterative solution

### Pseudocode

```
function Fib(n):
    1. f1 := 1
    2. f2 := 1
    3. From i := 3 to n + 1, do:
        4. f3 := f1 + f2
        5. f1 := f2
        6. f2 := f3
    7. Return f2
```

### Block diagram

```mermaid
flowchart TD
	START(["Fib(n)"]) --> K1[f1 := 1\nf2 := 1\ni := 3]
	K1 --> K3{i <= n + 1}
	K3 -- TRUE --> K4[f3 := f1 + f2\nf1 := f2\nf2 := f3\ni := i +1]
	K4 --> K3
	K3 -- FALSE --> K7[/Return f2/]
	K7 --> STOP([STOP])
```

## Implementation

### C++

{% content-ref url="../../programming/c++/algorithms/integers/fibonacci-numbers.md" %}
[fibonacci-numbers.md](../../programming/c++/algorithms/integers/fibonacci-numbers.md)
{% endcontent-ref %}

### Python

{% content-ref url="../../programming/python/algorithms/integers/fibonacci-numbers.md" %}
[fibonacci-numbers.md](../../programming/python/algorithms/integers/fibonacci-numbers.md)
{% endcontent-ref %}
