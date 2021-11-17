# Number game

## Description

Imagine a simple game played by children: there are several numbers given and the goal is to construct the largest number by joining them together.

For example, we can have three number: $$90$$, $$101$$ and $$3$$.
We can join them together to form another number: $$901013$$, $$903101$$, $$101903$$, $$101390$$, $$310190$$ and $$390101$$.
As you can see there are a total of $$6$$ combinations.
The largest number we can create that way is of course $$903101$$.
Your goal is to find such a largest number and win the game!.


Source: [https://onlinejudge.org/external/109/10905.pdf](https://onlinejudge.org/external/109/10905.pdf)

### Specification

#### Input

* $$n$$ - number of given integers
* $$a_1, a_2, ..., a_n$$ - $$n$$ integers

#### Output

* Largest number that can be obtained by joining together numbers $$a_1, a_2, ..., a_n$$ in some order

### Example 1

#### Input

```
4
123 124 56 90
```

#### Output

```
9056124123
```

### Example 2

#### Input

```
5
123 124 56 90 9 
```

#### Output

```
99056124123
```