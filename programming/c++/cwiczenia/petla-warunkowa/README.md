# Pętla warunkowa

## Zadanie 1

Napisz program zgodny z poniższą specyfikacją.

### Specification

#### Input

* $$n$$ - liczba naturalna

#### Output

* Kolejne cyfry liczby $$n$$, wypisane od końca, tzn. zaczynając od cyfry jedności

## Zadanie 2

Napisz program zgodny z poniższą specyfikacją.

### Specification

#### Input

* $$n$$ - liczba naturalna

#### Output

* Suma cyfr liczby $$n$$

### Example

#### Input

```
n := 1234
```

**Wynik**: $$10$$

{% hint style="info" %}
**Wyjaśnienie**

$$1+2+3+4=10$$ 
{% endhint %}

## Zadanie 3

Napisz program zgodny z poniższą specyfikacją.

### Specification

#### Input

* $$n$$ - liczba naturalna

#### Output

* Liczba powstała poprzez odwrócenie cyfr liczby $$n$$

### Example

#### Input

```
n := 1234
```

**Wynik**: $$4321$$

## Zadanie 4

Napisz program zgodny z poniższą specyfikacją.

### Specification

#### Input

* $$n$$ - liczba naturalna
* $$k$$ - liczba naturalna z zakresu $$[0,9]$$

#### Output

* Liczba powstała poprzez zastąpienie każdej cyfry liczby $$n$$ przez wartość bezwzględną różnicy liczby $$k$$ i danej cyfry

### Example

#### Input

```
n := 1234
k := 3
```

**Wynik**: $$2101$$

{% hint style="info" %}
Wyjaśnienie

$$|3-1|=2$$ 

$$|3-2|=1$$ 

$$|3-3|=0$$ 

$$|3-4|=1$$ 
{% endhint %}

## Zadanie 5

Napisz program zgodny z poniższą specyfikacją.

### Specification

#### Input

* $$n$$ - liczba naturalna

#### Output

* Zapis binarny liczby $$n$$

### Example

#### Input

```
n := 10
```

**Wynik**: $$1010$$

{% hint style="info" %}
**Wyjaśnienie**

$$10_{10}=1010_2$$ 
{% endhint %}

## Zadanie 6

Napisz program zgodny z poniższą specyfikacją.

### Specification

#### Input

* $$n$$ - liczba naturalna
* $$p$$ - liczba naturalna z zakresu $$[2,9]$$

#### Output

* Zapis liczby $$n$$ w systemie o podstawie $$p$$ 

### Example

#### Input

```
n := 10
p := 3
```

**Wynik**: $$101$$

{% hint style="info" %}
**Wyjaśnienie**

$$10_{10}=101_3$$ 
{% endhint %}
