# Test doskonałości

## Problem description

Czym jest liczba doskonała? Zacznijmy od dwóch definicji.

{% hint style="info" %}
#### Liczba doskonała

Liczba doskonała to taka, która jest równa sumie wszystkich swoich **dzielników właściwych**.
{% endhint %}

{% hint style="info" %}
**Dzielnik właściwy**

Dzielnik liczby **różny** od niej samej.
{% endhint %}

Podobnie jak w przypadku testu pierwszości, problem doskonałości liczby jest podobny do problemu znalezienia wszystkich dzielników liczby, opisanego tutaj: [Wszystkie dzielniki](wszystkie-dzielniki.md)

Zaczynamy od formalnej specyfikacji i przykładu.

### Specification

#### Input:

* $$n$$ - liczba naturalna

#### Output:

* **PRAWDA **- jeżeli $$n$$ jest liczbą doskonałą
* **FAŁSZ **- jeżeli $$n$$ nie jest liczbą doskonałą

### Example 1

#### Input

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

### Example 2

#### Input

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

## Naive solution

Tym razem pominiemy rozwiązanie zupełnie naiwne i zaczniemy od naiwnego. Będziemy więc przechodzić przez kolejne wartości od $$1$$ do połowy naszej liczby. Tym razem nie chcemy ich wypisywać, tylko zsumować. Potrzebna więc nam będzie dodatkowa zmienna, do której będziemy dodawać kolejne dzielniki. Oczywiście taką zmienną musimy utworzyć **przed pętlą**. Jaką wartość początkową należy jej nadać? Jak to zwykle bywa, sumowanie zaczynamy od zera.

W pętli, gdy znajdziemy kolejny dzielnik, to dodajemy go do sumy. Na końcu, gdy już zsumujemy wszystkie dzielniki, czyli po wyjściu z pętli, należy sprawdzić, jaki wynik powinniśmy zwrócić. W tym celu porównujemy obliczoną sumę ze sprawdzaną liczbą. Jeżeli są sobie równe, to znaczy, że mamy do czynienia z liczbą doskonałą, więc zwracamy wynik PRAWDA. Jeżeli są od siebie różne, to liczba nie jest doskonała, więc zwracamy FAŁSZ.

Teraz możemy zapisać nasz algorytm.

### Pseudocode

```
funkcja CzyDoskonala(n):
    1. suma := 0
    2. Od i := 1 do n div 2, wykonuj:
        3. Jeżeli (n mod i) = 0, to:
            4. suma := suma + i
      
    5. Jeżeli suma = n, to:
        6. Zwróć PRAWDA, zakończ
   
    7. w przeciwnym przypadku:
        8. Zwróć FAŁSZ, zakończ
```

### Complexity

$$O(\frac{n}{2})$$

## Optimal solution

TODO

### Pseudocode

```
funkcja CzyDoskonala(n)
    1. suma := 1
    2. Od i := 2 do sqrt(n), wykonuj:
        3. Jeżeli (n mod i) = 0, to:
            4. suma := suma + i
            5. Jeżeli (n / i) != i, to:
                6. suma := suma + (n / i)
            
    7. Jeżeli suma = n, to:
        8. Zwróć PRAWDA, zakończ
    
    9. w przeciwnym przypadku:
        10. Zwróć FAŁSZ, zakończ
```

{% hint style="info" %}
**sqrt** oznacza pierwiastek
{% endhint %}

### Complexity

$$O(\sqrt{n})$$ 

## Implementation

### C++

{% content-ref url="../../programming/c++/algorithms/algorytmy-na-liczbach-calkowitych/test-doskonalosci.md" %}
[test-doskonalosci.md](../../programming/c++/algorithms/algorytmy-na-liczbach-calkowitych/test-doskonalosci.md)
{% endcontent-ref %}

### Python

{% content-ref url="../../programming/python/algorithms/algorytmy-na-liczbach-calkowitych/test-doskonalosci.md" %}
[test-doskonalosci.md](../../programming/python/algorithms/algorytmy-na-liczbach-calkowitych/test-doskonalosci.md)
{% endcontent-ref %}
