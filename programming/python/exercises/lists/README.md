# Lists

## Exercise 1

Write a program according to the specification below.

### Specification

#### Input

* $$n$$ - natural number
* $$a_1,a_2,\dots,a_n$$ - $$n$$ integers

#### Output

* $$a_n,a_{n-1},\dots,a_2,a_1$$ - given numbers in reverse order

### Example

#### Input

```
n := 5
a1 := 1
a2 := 2
a3 := 3
a4 := 4
a5 := 5
```

**Output**: $$5, 4, 3, 2, 1$$ 

## Exercise 2

Write a program according to the specification below.

### Specification

#### Input

* $$n$$ - natural number
* $$a_1,a_2,\dots,a_n$$ - $$n$$ integers
* $$k$$ - natural number, $$1<=k<=n$$

#### Output

* $$a_k$$ - $$k$$-th given number

### Example

#### Input

```
n := 5

a1 := 8
a2 := 3
a3 := 9
a4 := 1
a5 := 2

k := 3
```

**Output**: $$9$$ 

{% hint style="info" %}
**Explanation**

$$k := 3$$, and the third value given is $$9$$ (a3 := 9). 
{% endhint %}

## Exercise 3

Write a program according to the specification below.

### Specification

#### Input

* $$n$$ - natural number
* $$a_1,a_2,\dots,a_n$$ - $$n$$ integers
* $$p, k$$ - two natural numbers, $$1<=p,k<=n$$, $$p <= k$$

#### Output

* $$a_p+a_{p+1}+a_{p+2}+...+a_{k}$$ - sum of values at positions from $$p$$ to $$k$$

### Example

#### Input

```
n := 5

a1 := 8
a2 := 3
a3 := 9
a4 := 1
a5 := 2

p := 3
k := 5
```

**Output**: $$12$$ 

{% hint style="info" %}
**Explanation**

$$a_3+a_4+a_5=9+1+2=12$$
{% endhint %}

## Exercise 4

Write a program according to the specification below.

### Specification

#### Input

* $$n$$ - natural number
* $$t1[n],\ t2[n]$$ - two lists of integers

#### Output

* The list created by adding a values from lists $$t1$$ and $$t2$$

### Example

#### Input

```
n := 5
t1 := [4, 1, 7, 0, 2]
t2 := [2, 3, 1, 9, 6]
```

**Output**: $$6, 4, 8, 9, 8$$ 

{% hint style="info" %}
**Explanation**

$$[4+2,\ 1+3,\ 7+1,\ 0+9,\ 2+6]$$ 
{% endhint %}

## Exercise 5

Write a program according to the specification below.

### Specification

#### Input

* $$n$$ - natural number

#### Output

* $$fib[n]$$ - list containing $$n$$ consecutive Fibonacci numbers

### Example

#### Input

```
n := 6
```

**Output**: $$1, 1, 2, 3, 5, 8$$ 

## Exercise 6

Write a program according to the specification below.

### Specification

#### Input

* $$n$$ - natural number

#### Output

* $$mult[n][n]$$ - a two-dimensional array representing a multiplication table in the range $$[0,n-1]$$, where $$mult[i][j]=i*j$$

### Example

#### Input

```
n := 3
```

#### Output

```
mno := [[0, 0, 0],
        [0, 1, 2],
        [0, 2, 4]]
```

## Exercise 7

Write a program according to the specification below.

### Specification

#### Input

* $$n$$ - natural number
* $$tab[n]$$ - integers list

#### Output

* "Ascending" message if the list elements are sorted in ascending order
* "Descending" message if the list elements are sorted in descending order
* "Unsorted" message if the list elements are not sorted

### Example 1

#### Input

```
n := 5
tab := [1, 1, 5, 6, 8]
```

**Output**: "Ascending"

### Example 2

#### Input

```
n := 5
tab := [8, 5, 5, 3, 1]
```

**Output**: "Descending"

### Example 3

#### Input

```
n := 5
tab := [1, 2, 3, 1, 5]
```

**Output**: "Unsorted"

## Exercise 8

Write a program according to the specification below.

### Specification

#### Input

* $$n$$ - natural number
* $$p, k$$ - two natural numbers, $$p <= k$$

#### Output

* $$n$$-elements list filled with random values from the range $$[p, k]$$