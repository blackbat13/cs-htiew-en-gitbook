# Kod ASCII

## Opis problemu

{% content-ref url="../../../../algorithms/kompresja/kod-ascii.md" %}
[kod-ascii.md](../../../../algorithms/kompresja/kod-ascii.md)
{% endcontent-ref %}

## Podstawowa tablica ASCII

### Implementation

```python
for i in range(128):
    print(chr(i))
```

### Link do implementacji

{% embed url="https://ideone.com/hwYbpz" %}
Podstawowa tablica ASCII
{% endembed %}

### Opis implementacji

Podstawowa tablica ASCII zawiera 128 znaków numerowanych od zera. Przechodzimy więc pętlą od 0 do 127 włącznie (**linia 1**) i, korzystając z funkcji `chr` zamieniającej liczbę na odpowiadający jej znak z tablicy ASCII, wypisujemy kolejne znaki (**linia 2**).

## Rozszerzona tablica ASCII

### Implementation

```python
for i in range(256):
    print(chr(i))
```

### Link do implementacji

{% embed url="https://ideone.com/1fn3jX" %}
Rozszerzona tablica ASCII
{% endembed %}

### Opis implementacji

Rozszerzona tablica ASCII zawiera 256 znaków numerowanych od zera. Przechodzimy więc pętlą od 0 do 255 włącznie (**linia 1**) i, korzystając z funkcji `chr` zamieniającej liczbę na odpowiadający jej znak z tablicy ASCII, wypisujemy kolejne znaki (**linia 2**).

