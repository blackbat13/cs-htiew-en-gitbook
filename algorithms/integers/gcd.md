# Euclid's algorithm

## Problem description

### Specification

#### Input

* $$a, b$$ — natural numbers, $$a>0$$, $$b>0$$

#### Output

* $$GCD(a, b)$$ — greatest common divisor of numbers $$a$$ and $$b$$ 

### Example

#### Input

```
a := 32
b := 12
```

**Output**: $$4$$ 

{% hint style="info" %}
**Explanation**

Divisors of the number $$32$$: $$1, 2, 4, 8, 16, 32$$

Divisors of the number $$12$$: $$1, 2, 3, 4, 6, 12$$

Common divisors: $$1, 2, 4$$ 

The greatest of them is $$4$$.
{% endhint %}

## Subtraction method

### Pseudocode

```
function GCD(a, b):
    1. While a != b, do:
        2. If a > b, then:
            3. a := a - b
        4. else:
            5. b := b - a
    6. Return a
```

### Block diagram

```mermaid
flowchart TD
	START(["GCD(a, b)"]) --> K1{a != b}
	K1 -- TRUE --> K2{a > b}
	K2 -- TRUE --> K3[a := a - b]
	K3 --> K1
	K2 -- FALSE --> K5[b := b - a]
	K5 --> K1
	K1 -- FALSE --> K6[/Return a/]
	K6 --> STOP([STOP])
```

## Iterative modulo method

### Pseudocode

```
function GCD(a, b):
    1. While b != 0, do:
        2. b2 := b
        3. b := a mod b
        4. a := b2
    5. Return a
```

{% hint style="info" %}
**mod** stands for modulo
{% endhint %}

### Block diagram

```mermaid
flowchart TD
	START(["GCD(a, b)"]) --> K1{b != 0}
	K1 -- TRUE --> K2[b2 := b\nb := a mod b\na := b2]
	K2 --> K1
	K1 -- FALSE --> K5[/Return a/]
	K5 --> STOP([STOP])
```

## Recursive modulo method

### Pseudocode

```
function GCD(a, b):
    1. If b = 0, then:
        2. Return a
    3. Return GCD(b, a mod b)
```

### Block diagram

```mermaid
flowchart TD
	START(["GCD(a, b)"]) --> K1{b = 0}
	K1 -- TRUE --> K2[/Return a/]
	K2 --> STOP([STOP])
	K1 -- FALSE --> K3[/"Return GCD(b, a mod b)"/]
	K3 --> STOP
```

## Implementation

### C++

{% content-ref url="../../programming/c++/algorithms/integers/gcd.md" %}
[gcd.md](../../programming/c++/algorithms/integers/gcd.md)
{% endcontent-ref %}

### Python

{% content-ref url="../../programming/python/algorithms/integers/gcd.md" %}
[gcd.md](../../programming/python/algorithms/integers/gcd.md)
{% endcontent-ref %}

### Blockly

{% content-ref url="../../programming/blockly/algorithms/integers/gcd.md" %}
[gcd.md](../../programming/blockly/algorithms/integers/gcd.md)
{% endcontent-ref %}

