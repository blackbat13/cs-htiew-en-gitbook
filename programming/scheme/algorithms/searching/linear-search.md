# Wyszukiwanie liniowe

## Problem description

{% content-ref url="../../../../algorithms/searching/linear-search.md" %}
[linear-search.md](../../../../algorithms/searching/linear-search.md)
{% endcontent-ref %}

## Istnienie elementu

### Implementation

{% code overflow="wrap" lineNumbers="true" %}
```scheme
(define linearSearch
  (lambda (array number)
    (if (null? array)
        #f
    (if (= (car array) number)
        #t
    (linearSearch (cdr array) number)
    ))
  )
)

(display (linearSearch `(8 2 9 10 5 4 2 7 18 0) 7))
```
{% endcode %}

### Link do implementacji

{% embed url="https://ideone.com/ZH8p3V" %}
Wyszukiwanie liniowe - istnienie elementu
{% endembed %}

### Implementation description

Funkcja `linearSearch` (**linia 1**) zwraca jako wynik wartość prawda/fałsz (`#t`/`#f`) i przyjmuje dwa argumenty: listę do przeszukania oraz wartość poszukiwanego elementu. Na początku funkcji sprawdzamy, czy lista jest pusta (**linia 3**). Jeżeli tak, to zwracamy wartość `#f` informującą o tym, że poszukiwanego elementu nie znaleziono w liście i kończymy działanie (**linia 4**). Jest to tzw. warunek stopu rekurencji. Jeżeli na liście pozostały jeszcze jakieś elementy do sprawdzenia, to sprawdzamy, czy pierwszy element listy (pobrany za pomocą funkcji `car`) jest poszukiwaną wartością (**linia 5**). Jeżeli tak, to zwracamy wynik `#t` (**linia 6**). W przeciwnym przypadku wywołujemy rekurencyjnie funkcję `linearSearch`, jako argumenty przekazując listę bez pierwszego elementu (do tego używamy funkcji `cdr`), oraz wartość poszukiwanego elementu.

W części głównej programu na wywołujemy funkcję `linearSearch` z przygotowanymi parametrami i jej wynik wyświetlamy na ekranie za pomocą funkcji `display` (**linia 12**).

## Pozycja elementu

### Implementation

{% code overflow="wrap" lineNumbers="true" %}
```scheme
(define linearSearch
  (lambda (array number index)
    (if (null? array)
        -1
    (if (= (car array) number)
        index
    (linearSearch (cdr array) number (+ index 1))
    ))
  )
)
 
(display (linearSearch `(8 2 9 10 5 4 2 7 18 0) 4 0))
```
{% endcode %}

### Link do implementacji

{% embed url="https://ideone.com/hNjuQ3" %}
Wyszukiwanie liniowe - pozycja elementu
{% endembed %}

### Implementation description

Funkcja `linearSearch` (**linia 1**) zwraca jako wynik wartość liczbę całkowitą i przyjmuje trzy argumenty: listę do przeszukania, wartość poszukiwanego elementu oraz numer obecnie sprawdzanego indeksu. Na początku funkcji sprawdzamy, czy lista jest pusta (**linia 3**). Jeżeli tak, to zwracamy wartość `-1` informującą o tym, że poszukiwanego elementu nie znaleziono w liście i kończymy działanie (**linia 4**). Jest to tzw. warunek stopu rekurencji. Jeżeli na liście pozostały jeszcze jakieś elementy do sprawdzenia, to sprawdzamy, czy pierwszy element listy (pobrany za pomocą funkcji `car`) jest poszukiwaną wartością (**linia 5**). Jeżeli tak, to zwracamy jako wynik wartość `index` zawierającą indeks aktualnie sprawdzanego elementu (**linia 6**). W przeciwnym przypadku wywołujemy rekurencyjnie funkcję `linearSearch`, jako argumenty przekazując listę bez pierwszego elementu (do tego używamy funkcji `cdr`), wartość poszukiwanego elementu oraz indeks zwiększony o jeden.

W części głównej programu na wywołujemy funkcję `linearSearch` z przygotowanymi parametrami i jej wynik wyświetlamy na ekranie za pomocą funkcji `display` (**linia 12**).