# Sequence differences

## Description

A sequence of $$n$$ integers is given.
Your goal is to check whether if we take the absolute values of differences between each two subsequent sequence elements, we will receive all numbers from the range $$1$$ to $$n-1$$ inclusive.

Source: [https://onlinejudge.org/external/100/10038.pdf](https://onlinejudge.org/external/100/10038.pdf)

### Specification

#### Input

* $$n$$ - natural number from the range $$[1,3000]$$
* $$tab[n]$$ - sequence of $$n$$ integers

#### Output

* "YES" If the sequence meets the requirement described above, or "NO" otherwise

### Example 1

#### Input

```
4
1 4 2 3
```

#### Output

```
YES
```

{% hint style="info" %}
#### Explanation

Let's look at the absolute values of differences between neighboring elements of sequence:

* $$|1-4|=3$$ 
* $$|4-2|=2$$ 
* $$|2-3|=1$$ 

As you can see, we have received all values from $$[1, N-1]$$, i.e. from $$[1,3]$$.
{% endhint %}

### Example 2

#### Input

```
5
1 4 2 -1 6
```

#### Output

```
NO
```

{% hint style="info" %}
#### Explanation

Let's look at the absolute values of differences between neighboring elements of sequence:

* $$|1-4|=3$$ 
* $$|4-2|=2$$ 
* $$|2-(-1)|=3$$ 
* $$|-1-6|=7$$ 

As you can see, we have not received all values from $$[1, N-1]$$, i.e. from $$[1,4]$$
{% endhint %}
