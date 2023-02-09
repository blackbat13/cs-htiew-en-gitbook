# Sale

## Description

In Topolandi, farmer Włodzimir lives. 
Włodzimir sales milk from his cows.
Recently, he decided to start a special sale: for $$3$$ empty milk bottles you can get $$1$$ full bottle of milk for FREE!
How many milk bottles can you drink if you have already purchased $$n$$ bottles of milk?

Ps. Mr. Włodzimir will be happy to borrow you empty bottles if you return them later.

Source: [https://onlinejudge.org/external/111/11150.pdf](https://onlinejudge.org/external/111/11150.pdf)

### Specification

#### Input

* $$n$$ - number of purchased milk bottles from the range $$[1,200]$$

#### Output

* The maximum number of milk bottles that can be drunk using the sale.

### Example

#### Input

```
8
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
