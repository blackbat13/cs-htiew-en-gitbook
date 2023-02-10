# ASCII codes

## Problem description

{% content-ref url="../../../../algorithms/coding-and-compression/ascii.md" %}
[ascii.md](../../../../algorithms/coding-and-compression/ascii.md)
{% endcontent-ref %}

## Standard ASCII table

### Implementation

{% code overflow="wrap" lineNumbers="true" %}
```python
for i in range(128):
    print(chr(i))
```
{% endcode %}

### Implementation description

Podstawowa tablica ASCII zawiera 128 znaków numerowanych od zera. Przechodzimy więc pętlą od 0 do 127 włącznie (**linia 1**) i, korzystając z funkcji `chr` zamieniającej liczbę na odpowiadający jej znak z tablicy ASCII, wypisujemy kolejne znaki (**linia 2**).

## Extended ASCII table

### Implementation

{% code overflow="wrap" lineNumbers="true" %}
```python
for i in range(256):
    print(chr(i))
```
{% endcode %}

### Implementation description

Rozszerzona tablica ASCII zawiera 256 znaków numerowanych od zera. Przechodzimy więc pętlą od 0 do 255 włącznie (**linia 1**) i, korzystając z funkcji `chr` zamieniającej liczbę na odpowiadający jej znak z tablicy ASCII, wypisujemy kolejne znaki (**linia 2**).
