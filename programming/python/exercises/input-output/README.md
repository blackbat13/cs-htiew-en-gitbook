# Handling the input/output

## Exercise 1

Write a program that complies with the specification below.

### Specification

#### Input

* $$name$$ - string of characters, upper and lower case letters of the English alphabet

#### Output

* A greeting message in the form of "**Hello \[name]!**"

### Example

#### Input

```
name := "Damian"
```

**Output**: "Hello Damian!"

## Exercise 2

Write a program that complies with the specification below

### Specification

#### Input

* $$a, b$$ - two integers

#### Output

* Sum of $$a$$ and $$b$$ 

### Example

#### Input

```
a := 2
b := 3
```

**Output**: $$5$$ 

## Exercise 3

Write a program that complies with the specification below

### Specification

#### Input

* $$a, b$$ - two non-zero integers

#### Output

* The result of dividing numbers $$a$$ and $$b$$ 

### Example

#### Input

```
a := 1
b := 2
```

**Output**: $$0.5$$ 

## Exercise 4

Write a program that complies with the specification below

### Specification

#### Input

* $$a, b$$ - two integers, greater than zero

#### Output

* The result of an integer division and the remainder of the division of numbers $$a$$ and $$b$$ 

### Example

#### Input

```
a := 7
b := 3
```

**Output**: $$2$$, remainder$$1$$ 

## Exercise 5

Write a program that complies with the specification belowWrite a program that complies with the specification below

{% hint style="info" %}
**Hint**

Use the **sqrt** function from the **math** library.
{% endhint %}

### Specification

#### Input

* $$a$$ - natural number

#### Output

* The root of $$a$$

### Example

#### Input

```
a := 4
```

**Output**: $$2$$ 

## Exercise 6

Write a program that complies with the specification below. Use the **min **function.

### Specification

#### Input

* $$a, b$$ - two integers

#### Output

* The smaller of the numbers $$a$$ and $$b$$, or any number, when they are equal to each other

### Example

#### Input

```
a := 5
b := 3
```

**Output**: $$3$$ 

## Exercise 7

Write a program that complies with the specification below. Use the **max **function.

### Specification

#### Dane

* $$a, b, c$$ - three integers

#### Wynik

* The largest of the numbers $$a$$, $$b$$ and $$c$$, or any when they are equal

### Example

#### Input

```
a := 3
b := 1
c := 3
```

**Output**: $$3$$ 

## Example 8

Write a program that complies with the specification below.

### Specification

#### Input

* $$seconds$$ - natural number

#### Output

* Time given in a legible form $$H:M:S$$ ($$H$$ - hours, $$M$$ - minutes, $$S$$ - seconds)

### Example

#### Input

```
seconds := 9179
```

**Output**: $$2:32:59$$ 

{% hint style="info" %}
**Explanation**

$$2H=7200S$$ 

$$32M=1920S$$ 

$$2H+32M+59S=7200S+1920S+59S=9179S$$ 
{% endhint %}