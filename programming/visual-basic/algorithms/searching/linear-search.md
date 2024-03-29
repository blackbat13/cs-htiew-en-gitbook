# Wyszukiwanie liniowe

## Problem description

{% content-ref url="../../../../algorithms/searching/linear-search.md" %}
[linear-search.md](../../../../algorithms/searching/linear-search.md)
{% endcontent-ref %}

## Istnienie elementu

### Implementation

{% code overflow="wrap" lineNumbers="true" %}
```visual-basic
Module Search
    Public Function LinearSearch(array as Integer(), number as Integer) As Boolean
        For Each el As Integer In array
            If el = number Then
                Return True
            End If
        Next
    
        Return False
    End Function
    
    Sub Main()
        Dim array as Integer() = {4, 8, 1, 3, 8, 0, 2, 5, 2}
        Dim number as Integer = 0

        Dim result as Boolean = LinearSearch(array, number)

        If result Then
            Console.WriteLine("Liczba jest w tablicy")
        Else
            Console.WriteLine("Liczby nie ma w tablicy")
        End If
    End Sub
End Module
```
{% endcode %}

### Link do implementacji

{% embed url="https://ideone.com/E4ItjS" %}
Wyszukiwanie liniowe - istnienie elementu
{% endembed %}

## Pozycja elementu

### Implementation

{% code overflow="wrap" lineNumbers="true" %}
```visual-basic
Module Search
    Public Function LinearSearch(array as Integer(), number as Integer) As Integer
        For index As Integer = 0 To array.Length - 1
            If array(index) = number Then
                Return index
            End If
        Next
    
        Return -1
    End Function
    
    Sub Main()
        Dim array as Integer() = {4, 8, 1, 3, 8, 0, 2, 5, 2}
        Dim number as Integer = 0

        Dim index as Integer = LinearSearch(array, number)

        If index = -1 Then
            Console.WriteLine("Liczby nie ma w tablicy")
        Else
            Console.WriteLine("Liczba jest w tablicy pod indeksem {0}", index)
        End If
    End Sub
End Module
```
{% endcode %}

### Link do implementacji

{% embed url="https://ideone.com/slBT8K" %}
Wyszukiwanie liniowe - pozycja elementu
{% endembed %}

## Wszystkie pozycje elementu

### Implementation

{% code overflow="wrap" lineNumbers="true" %}
```visual-basic
Module Search
    Public Sub LinearSearch(array as Integer(), number as Integer)
        For index As Integer = 0 To array.Length - 1
            If array(index) = number Then
                Console.WriteLine(index)
            End If
        Next
    End Sub
    
    Sub Main()
        Dim array as Integer() = {4, 8, 1, 3, 8, 0, 2, 5, 8}
        Dim number as Integer = 8

        Console.WriteLine("Indeksy, pod którymi znajduje się szukana liczba:")

        LinearSearch(array, number)
    End Sub
End Module
```
{% endcode %}

### Link do implementacji

{% embed url="https://ideone.com/LkA3ln" %}
Wyszukiwanie liniowe - wszystkie pozycje elementu
{% endembed %}