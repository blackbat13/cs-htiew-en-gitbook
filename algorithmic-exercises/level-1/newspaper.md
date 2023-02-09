# Newspaper

## Description

The Bitek newspaper in Bajtkowo is very popular, even in its original paper version.
As a result, many people send their ads to the editorial office to place them in the next issue.
Until now, the rate has been clear: a fixed amount for each advertisement, depending on the number of characters.
The publisher of the Bitek newspaper noticed, however, that different signs consume different amounts of ink, which means that the cost of their print is also different!
So he decided to update the price list and determine the cost of each sign. Now the message fee is equal to the sum of the costs of each sign from the message.

Your task is to count the fee for a given message according to the new price list.


Source: [https://onlinejudge.org/external/113/11340.pdf](https://onlinejudge.org/external/113/11340.pdf)

### Specification

#### Input

* $$n$$ - number of characters
* $$(z_1, c_1), (z_2, c_2), ..., (z_n, c_n)$$ - price list: pair of the character and the price of that character, given in pennies
* $$word$$ - a string of characters, small and/or capital letters of the English alphabet, without spaces and other white characters

#### Output

* Fee for the $$word$$, given in zlotys, according to the new price list. We assume that every character from the message will appear in the price list.

### Example

#### Input

```
6
a 5
l 25
m 30
k 50
o 10
t 1
alamakota
```

#### Output

```
1.36
```

{% hint style="info" %}
#### Explanation

In a word **alamakota** we can distinguish:

* $$4$$ letters **a**
* $$1$$ letter **l**
* $$1$$ letter **m**
* $$1$$ letter **k**
* $$1$$ letter **o**
* $$1$$ letter **t**

It gives us:
$$4*5+1*25+1*30+1*50+1*10+1*1=136$$ pens, that is $$1.36$$ zloty.
{% endhint %}