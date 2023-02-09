# Algorytm Euklidesa

## Opis problemu

TODO

### Specyfikacja

#### Dane

* $$a, b$$ — liczby naturalne, większe od zera

#### Wynik

* $$NWD(a, b)$$ — największy wspólny dzielnik liczb $$a$$ i $$b$$ 

### Przykład

#### Dane

```
a := 32
b := 12
```

**Wynik**: $$4$$ 

{% hint style="info" %}
**Wyjaśnienie**

Dzielnikami liczby $$32$$ są: $$1, 2, 4, 8, 16, 32$$

Dzielnikami liczby $$12$$ są: $$1, 2, 3, 4, 6, 12$$

Wspólnymi dzielnikami są więc: $$1, 2, 4$$ 

Największy z nich to właśnie $$4$$.
{% endhint %}

## Wersja z odejmowaniem

### Pseudokod

```
function GCD(a, b):
    1. While a != b, do:
        2. If a > b, then:
            3. a := a - b
        4. else:
            5. b := b - a
    6. Return a
```

### Schemat blokowy

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

## Wersja z modulo — iteracyjna

### Pseudokod

```
function GCD(a, b):
    1. While b != 0, do:
        2. b2 := b
        3. b := a mod b
        4. a := b2
    5. Return a
```

{% hint style="info" %}
**mod** oznacza resztę z dzielenia
{% endhint %}

### Schemat blokowy

```mermaid
flowchart TD
	START(["GCD(a, b)"]) --> K1{b != 0}
	K1 -- TRUE --> K2[b2 := b\nb := a mod b\na := b2]
	K2 --> K1
	K1 -- FALSE --> K5[/Return a/]
	K5 --> STOP([STOP])
```

## Wersja z modulo — rekurencyjna

### Pseudokod

```
function GCD(a, b):
    1. If b = 0, then:
        2. Return a
    3. Return GCD(b, a mod b)
```

### Schemat blokowy

```mermaid
flowchart TD
	START(["GCD(a, b)"]) --> K1{b = 0}
	K1 -- TRUE --> K2[/Return a/]
	K2 --> STOP([STOP])
	K1 -- FALSE --> K3[/"Return GCD(b, a mod b)"/]
	K3 --> STOP
```

## Implementacja

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

