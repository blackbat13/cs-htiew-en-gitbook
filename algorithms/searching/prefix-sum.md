# Sumy prefiksowe

## Problem description

Czasami bywa tak, że musimy policzyć **sumę pewnego spójnego fragmentu tablicy**, a nawet kilku. Jak to zrobić w sposób efektywny? Jeżeli z**awartość tablicy nie będzie ulegała zmianom**, to z pomocą przyjdą nam **sumy prefiksowe**.

### Specification

#### Input

* $$n$$ — liczba naturalna, liczba elementów tablicy.
* $$A[1..n]$$ — $$n-elementowa$$ tablica liczb całkowitych, indeksowana od jedynki.
* $$m$$ — liczba naturalna, liczba zapytań.
* $$P[1..m][1..2]$$ - dwuwymiarowa tablica liczb naturalnych z zakresu $$[1..n]$$, zapytań o sumy przedziałów, gdzie $$P[i][1]$$ to początek $$i$$-tego przedziału, a $$P[i][2]$$ to jego koniec.

#### Output

* $$m$$ liczb naturalnych, dla każdego zapytania $$i$$ suma wartości pod indeksami od $$P[i][1]$$ do $$P[i][2]$$, tzn. $$A[P[i][1]] + A[P[i][1] + 1] + A[P[i][1] + 2] + ... + A[P[i][2]]$$.

### Example

#### Input

```
n := 10
A[1..10] := [4, 8, 2, 6, 1, 0, 8, 4, 2, 3]
m := 3
P[1..3][1..2] := [[3, 5], [6, 7], [1, 1]]
```

#### Output

```
9
8
4
```

{% hint style="info" %}
**Wyjaśnienie**

* $$sum_1 = A[3] + A[4] + A[5] = 2 + 6 + 1 = 9$$
* $$sum_2 = A[6] + A[7] = 0 + 8 = 8$$
* $$sum_3 = A[1] = 4$$
{% endhint %}

## Naive solution

Rozwiązanie naiwne jest proste. Wystarczy dla każdego zapytania policzyć sumę przedziału przechodząc kolejno po elementach tablicy pod indeksami znajdującymi się w przedziale. Możemy to zrobić za pomocą zwykłej pętli iteracyjnej, dodając kolejne elementy tablicy do liczonej sumy.

### Pseudocode

```
function RangeSum(n, A, m, P):
    1. From i := 1 to m, do:
        2. sum := 0
        3. From j := P[i][1] to P[i][2], do:
            4. sum := sum + A[j]
        5. Print sum
```

### Block diagram

```mermaid
flowchart TD
	START(["RangeSum(n, A, m, P)"]) --> K0[i := 1]
	K0 --> K1{i <= m}
	K1 -- TRUE --> K2["sum := 0\nj := P[i][1]"]
	K2 --> K3{"j <= P[i][2]"}
	K3 -- TRUE --> K4["sum := sum + A[j]"]
	K4 --> K3i[j := j + 1]
	K3i --> K3
	K3 -- FALSE --> K5[/Print sum/]
	K5 --> K1i[i := i + 1]
	K1i --> K1
	K1 -- FALSE --> STOP([STOP])
```

## Optimal solution

### Pseudocode

```
function RangeSum(n, A, m, P):
    1. pref := [0..n]
    2. pref[0] := 0
    3. From i := 1 to n, do:
        4. pref[i] := pref[i - 1] + A[i]
    5. From i := 1 to m, do:
        6. sum := pref[P[i][2]] - pref[P[i][1] - 1]
        7. Print sum
```

### Block diagram

```mermaid
flowchart TD
	START(["RangeSum(n, A, m, P)"]) --> K1["pref := [0..n]\npref[0] := 0"]
	K1 --> K3{i <= n}
	K3 -- TRUE --> K4["pref[i] := pref[i - 1] + A[i]"]
    K4 --> K3i[i := i + 1]
    K3i --> K3
    K3 -- FALSE --> K5p[i := 1]
    K5p --> K5{i <= m}
    K5 -- TRUE --> K6["sum := pref[P[i][2]] - pref[P[i][1] - 1]"]
    K6 --> K7[/Print sum/]
    K7 --> K5i[i := i + 1]
    K5i --> K5
    K5 -- FALSE ----> STOP([STOP])
```