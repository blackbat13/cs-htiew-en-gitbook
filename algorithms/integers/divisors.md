# All divisors

## Problem description

Czasem bywa tak, że potrzebujemy poznać wszystkie **dzielniki** zadanej liczby. Dzielnik to wartość, przez którą liczba jest podzielna, czy też mówiąc inaczej, dzieli się bez reszty.

Zadanie to jest stosunkowo proste, należy jednak zadać sobie pytanie: **jakie liczby musimy sprawdzić, by znaleźć wszystkie dzielniki**? Jak zobaczymy, odpowiedź nie jest taka oczywista i do tego problemu można podejść na kilka sposobów. Zanim jednak przejdziemy do rozwiązań, zacznijmy od formalnej specyfikacji problemu i prostego przykładu.

### Specification

#### Input

* $$n$$ — liczba naturalna, większa od zera

#### Output

* Wszystkie dzielniki liczby $$n$$ 

### Example

#### Input

```
n := 12
```

**Wynik**: $$1,2,3,4,6,12$$ 

## Naive solution

Przejdźmy do próby rozwiązania problemu. Naszym zadaniem jest wypisać **wszystkie dzielniki** podanej wartości. Nie możemy żadnego pominąć. Spróbujmy więc odpowiedzieć na postawione wcześniej pytanie: **jakie liczby musimy sprawdzić**? Po pierwsze możemy łatwo zauważyć, że nie ma sensu sprawdzać wartości mniejszych niż $$1$$. Najmniejszy i zarazem pierwszy dzielnik to będzie zawsze liczba $$1$$. Od niej więc zaczynamy poszukiwanie dzielników. W którym miejscu jednak należy się zatrzymać? Cóż, na pewno nie ma sensu sprawdzać wartości większych od $$n$$. Liczba nie może być podzielna przez wartość od siebie większą!

Podsumowując wystarczy sprawdzić wszystkie liczby od $$1$$ do $$n$$, aby znaleźć dzielniki. W ten sposób otrzymaliśmy pierwsze, zgrubne ograniczenie naszego przeszukiwanego przedziału wartości. Dla każdej liczby z tego zakresu będziemy sprawdzać, czy jest ona dzielnikiem $$n$$.

Pozostaje jeszcze bardzo ważna kwestia: jak sprawdzić, czy jedna liczba jest dzielnikiem drugiej? Cóż, wystarczy sprawdzić, czy **dzielą się bez reszty**. Czy też, bardziej formalnie, **reszta z dzielenia wynosi **$$0$$.

Spróbujmy teraz to wszystko zapisać w formie algorytmu.

### Pseudocode

```
function Divisors(n):
    1. From i := 1 to n, do:
        2. If n mod i = 0, then:
            3. Print i
```

{% hint style="info" %}
**mod** oznacza resztę z dzielenia
{% endhint %}

### Block diagram

```mermaid
flowchart TD
	START(["Divisors(n)"]) --> K0[i := 1]
	K0 --> K1{i <= n}
	K1 -- TRUE --> K2{n mod i = 0}
	K2 -- TRUE --> K3[/Print i/]
	K3 --> K1i[i := i + 1]
	K2 -- FALSE --> K1i
	K1i --> K1
	K1 -- FALSE ----> STOP([STOP])
```

### Complexity

W naszym rozwiązaniu przechodzimy przez wszystkie kolejne wartości od $$1$$ do $$n$$. Dla zadanego $$n$$ mamy więc do sprawdzenia $$n$$ potencjalnych dzielników. Stąd też otrzymujemy złożoność:

$$O(n)$$ — liniowa

## Better solution

Mamy już pierwsze rozwiązanie naszego problemu. Zastanówmy się teraz, jak możemy je **zoptymalizować**, czyli usprawnić. Szczególnym fragmentem naszego rozwiązania, który aż prosi się o optymalizację, jest przeglądanie liczb od $$1$$ do $$n$$. Pomyślmy, jak możemy zawęzić ten zakres?

### Pseudocode

```
function Divisors(n):
    1. From i := 1 to n div 2, do:
        2. If n mod i = 0, then:
            3. Print i
    4. If n > 1, then:
        5. Print n
```

{% hint style="info" %}
**div** oznacza dzielenie całkowite
{% endhint %}

### Block diagram

```mermaid
flowchart TD
	START(["Divisors(n)"]) --> K0[i := 1]
	K0 --> K1{i <= n div 2}
	K1 -- TRUE --> K2{n mod i = 0}
	K2 -- TRUE --> K3[/Print i/]
	K3 --> K1i[i := i + 1]
	K2 -- FALSE --> K1i
	K1i --> K1
	K1 -- FALSE --> K4{n > 1}
	K4 -- TRUE --> K5[/Print n/]
	K5 --> STOP([STOP])
	K4 -- FALSE --> STOP
```

### Complexity

W naszym rozwiązaniu przechodzimy przez wszystkie kolejne wartości od $$1$$ do $$n/2$$. Dla zadanego $$n$$ mamy więc do sprawdzenia $$n/2$$ potencjalnych dzielników. Stąd też otrzymujemy złożoność:

$$O(\frac{n}{2})$$

## Optimal solution

### Pseudocode

```
function Divisors(n):
    1. From i := 1 to sqrt(n), do:
        2. If n mod i = 0, then:
            3. Print i
            4. If (n / i) != i, then:
                5. Print (n / i)
```

{% hint style="info" %}
**sqrt** oznacza pierwiastek
{% endhint %}

### Block diagram

```mermaid
flowchart TD
	START(["Divisors(n)"]) --> K0[i := 1]
	K0 --> K1{"i <= sqrt(n)"}
	K1 -- TRUE --> K2{n mod i = 0}
	K2 -- TRUE --> K3[/Print i/]
	K3 --> K4{"(n / i) != i"}
	K4 -- TRUE --> K5[/"Print (n / i)"/]
	K5 --> K1i[i := i + 1]
	K4 -- FALSE --> K1i
	K2 -- FALSE --> K1i
	K1i --> K1
	K1 -- FALSE ------> STOP([STOP])
```

### Complexity

W naszym rozwiązaniu przechodzimy przez wszystkie kolejne wartości od $$1$$ do $$\sqrt{n}$$. Dla zadanego $$n$$ mamy więc do sprawdzenia $$\sqrt{n}$$ potencjalnych dzielników. Stąd też otrzymujemy złożoność:

$$O(\sqrt{n})$$

## Implementation

### C++

{% content-ref url="../../programming/c++/algorithms/integers/divisors.md" %}
[divisors.md](../../programming/c++/algorithms/integers/divisors.md)
{% endcontent-ref %}

### Python

{% content-ref url="../../programming/python/algorithms/integers/divisors.md" %}
[divisors.md](../../programming/python/algorithms/integers/divisors.md)
{% endcontent-ref %}
