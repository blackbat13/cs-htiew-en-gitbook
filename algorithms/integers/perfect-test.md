# Test doskonałości

## Opis problemu

Czym jest liczba doskonała? Zacznijmy od dwóch definicji.

{% hint style="info" %}
#### Liczba doskonała

Liczba doskonała to taka, która jest równa sumie wszystkich swoich **dzielników właściwych**.
{% endhint %}

{% hint style="info" %}
**Dzielnik właściwy**

Dzielnik liczby **różny** od niej samej.
{% endhint %}

Podobnie jak w przypadku testu pierwszości, problem doskonałości liczby jest podobny do problemu znalezienia wszystkich dzielników liczby, opisanego tutaj: [Wszystkie dzielniki](divisors.md)

Zaczynamy od formalnej specyfikacji i przykładu.

### Specyfikacja

#### Dane:

* $$n$$ - liczba naturalna

#### Wynik:

* **PRAWDA **- jeżeli $$n$$ jest liczbą doskonałą
* **FAŁSZ **- jeżeli $$n$$ nie jest liczbą doskonałą

### Przykład 1

#### Dane

```
n := 6
```

**Wynik**: PRAWDA

{% hint style="info" %}
#### Wyjaśnienie

Dzielnikami właściwymi liczby $$6$$ są: $$1, 2, 3$$ 

Po ich zsumowaniu otrzymamy z powrotem liczbę $$6$$:

$$6=1+2+3$$ 
{% endhint %}

### Przykład 2

#### Dane

```
n := 8
```

**Wynik**: FAŁSZ

{% hint style="info" %}
#### Wyjaśnienie

Dzielnikami właściwymi liczby 8 są: $$1, 2,4$$ 

Po ich zsumowaniu otrzymamy liczbę $$7$$:

$$8\not=1+2+4$$ 
{% endhint %}

## Rozwiązanie naiwne

Tym razem pominiemy rozwiązanie zupełnie naiwne i zaczniemy od naiwnego. Będziemy więc przechodzić przez kolejne wartości od $$1$$ do połowy naszej liczby. Tym razem nie chcemy ich wypisywać, tylko zsumować. Potrzebna więc nam będzie dodatkowa zmienna, do której będziemy dodawać kolejne dzielniki. Oczywiście taką zmienną musimy utworzyć **przed pętlą**. Jaką wartość początkową należy jej nadać? Jak to zwykle bywa, sumowanie zaczynamy od zera.

W pętli, gdy znajdziemy kolejny dzielnik, to dodajemy go do sumy. Na końcu, gdy już zsumujemy wszystkie dzielniki, czyli po wyjściu z pętli, należy sprawdzić, jaki wynik powinniśmy zwrócić. W tym celu porównujemy obliczoną sumę ze sprawdzaną liczbą. Jeżeli są sobie równe, to znaczy, że mamy do czynienia z liczbą doskonałą, więc zwracamy wynik PRAWDA. Jeżeli są od siebie różne, to liczba nie jest doskonała, więc zwracamy FAŁSZ.

Teraz możemy zapisać nasz algorytm.

### Pseudokod

```
function IsPerfect(n):
    1. sum := 0
    2. From i := 1 to n div 2, do:
        3. If (n mod i) = 0, then:
            4. sum := sum + i
      
    5. If suma = n, then:
        6. Return TRUE
   
    7. else:
        8. Return FALSE
```

### Block diagram

```mermaid
flowchart TD
	START(["IsPerfect(n)"]) --> K1[sum := 0\ni := 1]
	K1 --> K2{i <= n div 2}
	K2 -- TRUE --> K3{"(n mod i) = 0"}
	K3 -- TRUE --> K4[sum := sum + i]
	K3 -- FALSE --> K2i[i := i + 1]
	K4 --> K2i
	K2i --> K2
	K2 -- FALSE --> K5{suma = n}
	K5 -- TRUE --> K6[/Return TRUE/]
	K6 --> STOP([STOP])
	K5 -- FALSE --> K8[/Return FALSE/]
	K8 --> STOP
```

### Złożoność

$$O(\frac{n}{2})$$

## Rozwiązanie optymalne

TODO

### Pseudokod

```
function IsPerfect(n)
    1. sum := 1
    2. From i := 2 to sqrt(n), do:
        3. If (n mod i) = 0, then:
            4. sum := sum + i
            5. If (n / i) != i, then:
                6. sum := sum + (n / i)
            
    7. If suma = n, then:
        8. Return TRUE
    
    9. else:
        10. Return FALSE
```

{% hint style="info" %}
**sqrt** oznacza pierwiastek
{% endhint %}

### Block diagram

```mermaid
flowchart TD
	START(["IsPerfect(n)"]) --> K1[sum := 1\ni := 2]
	K1 --> K2{"i <= sqrt(n)"}
	K2 -- TRUE --> K3{"(n mod i) = 0"}
	K3 -- TRUE --> K4[sum := sum + i]
	K4 --> K5{"(n / i) != i"}
	K5 -- TRUE --> K6["sum := sum + (n / i)"]
	K6 --> K2i[i := i + 1]
	K5 -- FALSE --> K2i
	K3 -- FALSE --> K2i
	K2i --> K2
	K2 -- FALSE --> K7{sum = n}
	K7 -- TRUE ---> K8[/Return TRUE/]
	K8 ---> STOP([STOP])
	K7 -- FALSE ---> K10[/Return FALSE/]
	K10 ---> STOP
```

### Złożoność

$$O(\sqrt{n})$$ 

## Implementacja

### C++

{% content-ref url="../../programming/c++/algorithms/integers/perfect-test.md" %}
[perfect-test.md](../../programming/c++/algorithms/integers/perfect-test.md)
{% endcontent-ref %}

### Python

{% content-ref url="../../programming/python/algorithms/integers/perfect-test.md" %}
[perfect-test.md](../../programming/python/algorithms/integers/perfect-test.md)
{% endcontent-ref %}
