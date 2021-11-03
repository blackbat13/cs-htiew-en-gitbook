# Pakowanie na wakacje

## Opis

Nareszcie wakacje! Czas gdzieś wyjechać. Najpierw jednak czas się spakować. Masz do dyspozycji jedną walizkę w kształcie prostopadłościanu o wymiarach $$20cm\times20cm\times20cm$$. Udało Ci się zebrać wszystkie potrzebne rzeczy w jeden mały pakunek, także o kształcie prostopadłościanu. Pytanie brzmi, czy zmieści się on do walizki? Nie chcesz nic uszkodzić, więc pakunek nie może wystawać i musi być ułożony bokami równolegle do boków walizki.

Źródło: [https://onlinejudge.org/external/123/12372.pdf](https://onlinejudge.org/external/123/12372.pdf)

### Specyfikacja

#### Input

* $$a, b, c$$ - liczby naturalne, wymiary pakunku, wszystkie z zakresu $$[1, 50]$$ 

#### Wynik

* Komunikat "TAK", jeżeli pakunek zmieści się walizce, lub komunikat "NIE" w przeciwnym przypadku

### Example 1

#### Input

```
a := 20
b := 20
c := 20
```

**Wynik**: "TAK"

### Example 2

#### Input

```
a := 1
b := 2
c := 21
```

**Wynik**: "NIE"

