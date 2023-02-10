# Wyszukiwanie binarne

## Problem description

W wielu przypadkach, gdy musimy coś znaleźć, np. książkę na półce w bibliotece, to będziemy mieć do czynienia z konkretnym porządkiem.
Książki mogą być ułożone według tematyki, **posortowane** po nazwisku autora i tytule.
Znacząco ułatwia to znalezienie pożądanej pozycji, ponieważ **wiemy, gdzie szukać**.

Tak samo jest też w świecie algorytmiki. Gdy pracujemy na danych **posortowanych**, to zazwyczaj możemy skonstruować efektywne algorytmy do rozwiązania problemu. 

Jak zwykle, zacznijmy od formalnej specyfikacji, by lepiej zrozumieć problem, z którym będziemy się mierzyć.

### Specification

#### Input:

* $$n$$ - natural number, $$n>0$$
* $$A[1..n]$$ - array of $$n$$ integers, sorted in ascending order
* $$k$$ - integer

#### Output:

* Index of value $$k$$ in the array $$A$$, or $$-1$$ if the value is not found

### Example

#### Input

```
n := 5
A := [1, 2, 5, 7, 9]
k := 7 
```

**Output**: $$4$$ 

## Iterative solution

Zacznijmy od wersji iteracyjnej. Na początku definiujemy początek i koniec przeszukiwanego przedziału. Jako początek przyjmujemy numer pierwszego elementu (czyli $$1$$), a jako koniec numer ostatniego elementu (czyli $$n$$). W pętli będziemy powtarzać przeszukiwanie tak długo, jak długo nasz zdefiniowany przez początek i koniec przedział będzie zawierał co najmniej jeden element. Inaczej mówiąc, powtarzamy tak długo, jak długo początek jest mniejszy od końca.

Wewnątrz pętli najpierw obliczamy środek przeszukiwanego przedziału. Następnie sprawdzamy, jak element znajdujący się na środku ma się do naszego poszukiwanego elementu. Jeżeli poszukiwane element jest większy od elementu, który mamy na środku, to znaczy, że należy szukać po prawej stronie od środka: przesuwamy więc początek naszego przedziału na prawo od środka. W przeciwnym przypadku, czyli gdy poszukiwany element jest mniejszy bądź równy elementowi na środku, oznacza to, że należy szukać po lewej stronie od środka (ale nie możemy wykluczyć też elementu na środku!). W związku z tym przesuwamy koniec przedziału na środek. 

Gdy już wyjdziemy z pętli pozostaje nam sprawdzić, czy znaleźliśmy poszukiwany element. Sprawdzamy, czy pod indeksem wskazującym na zmieniony początek (lub koniec) przedziału znajduje się poszukiwana wartość. Jeżeli tak, to zwracamy jako wynik ten indeks. W przeciwnym przypadku zwracamy $$-1$$.

### Pseudocode

```
function BinarySearch(n, A, k)
    1. beg := 1
    2. end := n
    3. While beg < end, do:
        4. mid := (beg + end) div 2
        
        5. If k > A[mid], then:
            6. beg := mid + 1
        
        7. else:
            8. end := mid

    9. If A[beg] = k, then:
        10. Return beg
    11. else:
        12. Return -1
```

{% hint style="info" %}
**div** oznacza dzielenie całkowite
{% endhint %}

### Block diagram

```mermaid
flowchart TD
	START(["BinarySearch(n, A, k)"]) --> O1[beg := 1\nend := n]
	O1 --> C1{beg < end}
	C1 -- TRUE --> O2["mid := (beg + end) div 2"]
	O2 --> C2{"k > A[mid]"}
	C2 -- TRUE --> O3[beg := mid + 1]
	O3 --> C1
	C2 -- FALSE --> O4[end := mid]
	O4 --> C1
	C1 -- FALSE --> C3{"A[beg] = k"}
	C3 -- TRUE --> R1[/Return beg/]
	R1 --> STOP([STOP])
	C3 -- FALSE --> R2[/Return -1/]
	R2 --> STOP
```

### Complexity

$$O(\log n)$$ - logarithmic

## Recursive solution

W rozwiązaniu rekurencyjnym zamiast rozmiaru tablicy podajemy początek i koniec przeszukiwanego przedziału. Zaczynamy od sprawdzenia warunku stopu rekurencji: poprawności przedziału. Następnie postępujemy podobnie jak w wersji iteracyjnej. Obliczamy środek przedziału i porównujemy element znajdujący się na środku z poszukiwaną wartością. W zależności od wyniku porównania wykonujemy wywołanie rekurencyjne odpowiednio modyfikując przeszukiwany przedział.

### Pseudocode

```
function BinarySearch(A, k, beg, end)
    1. If beg >= end, then:
        2. If A[beg] == k, then:
            3. Return beg
        4. else:
            5. Return -1
    
    6. mid := (beg + end) div 2
    
    7. If k > A[mid], then:
        8. Return SzukajBinarnie(A, k, mid + 1, end)
    
    9. else:
        10. Return SzukajBinarnie(A, k, beg, mid)
```

### Block diagram

```mermaid
flowchart TD
	START(["BinarySearch(A, k, beg, end)"]) --> K1{beg >= end}
	K1 -- TRUE --> K2{"A[beg] = k"}
	K2 -- TRUE --> K3[/Return beg/]
	K3 --> STOP([STOP])
	K2 -- FALSE --> K5[/Return -1/]
	K5 --> STOP
	K1 -- FALSE --> K6["mid := (beg + end) div 2"]
	K6 --> K7{"k > A[mid]"}
	K7 -- TRUE --> K8[/"Return BinarySearch(A, k, mid + 1, end)"/]
	K8 --> STOP
	K7 -- FALSE --> K9[/"Return BinarySearch(A, k, beg, mid)"/]
	K9 --> STOP
```

### Complexity 

$$O(\log n)$$ - logarithmic

## Implementation

### C++

{% content-ref url="../../programming/c++/algorithms/searching/binary-search.md" %}
[binary-search.md](../../programming/c++/algorithms/searching/binary-search.md)
{% endcontent-ref %}

### Python

{% content-ref url="../../programming/python/algorithms/searching/binary-search.md" %}
[binary-search.md](../../programming/python/algorithms/searching/binary-search.md)
{% endcontent-ref %}

### Blockly

{% content-ref url="../../programming/blockly/algorithms/searching/binary-search.md" %}
[binary-search.md](../../programming/blockly/algorithms/searching/binary-search.md)
{% endcontent-ref %}

### Kotlin

{% content-ref url="../../programming/kotlin/algorithms/searching/binary-search.md" %}
[binary-search.md](../../programming/kotlin/algorithms/searching/binary-search.md)
{% endcontent-ref %}