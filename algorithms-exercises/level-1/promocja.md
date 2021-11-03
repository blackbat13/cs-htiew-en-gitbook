# Sale

## Description

In Topolandi, farmer Włodzimir lives. 
Włodzimir deals in the sale of milk, obtained from his cows.
Recently, he decided to apply a special promotion: for $$3$$ empty milk bottles you can get $$1$$ full bottle of milk FREE!
How many milk bottles can you drink using this promotion if you have already purchased $$n$$ bottles of milk?

Ps. Mr. Włodzimir will be happy to borrow you empty bottles if you return them later.

Source: [https://onlinejudge.org/external/111/11150.pdf](https://onlinejudge.org/external/111/11150.pdf)

### Specification

#### Input

* $$n$$ - liczba zakupionych butelek mleka z przedziału$$[1,200]$$

#### Output

* Maksymalna liczba butelek mleka , które można wypić, korzystając z promocji. 

### Example

#### Input

```
n := 8
```

#### Output

```
12
```

{% hint style="info" %}
#### Explanation

At the beginning, we have $$8$$ full of milk bottles.
If we borrow one empty bottle, then we can have $$9$$ empty bottles exchanged for $$3$$ new.
Drink $$3$$ bottles of milk and exchange them for one bottle of milk. 
We drink it, and at the end we return an empty bottle.
So we drank $$8$$, then $$3$$ and at the end $$1$$ bottle of milk:

$$8+3+1=12$$ 
{% endhint %}
