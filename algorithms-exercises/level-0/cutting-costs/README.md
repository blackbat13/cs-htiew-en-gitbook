# Cost cutting

## Description

A company decided to reduce employment. The goal is to cut costs. Employees work in three-person teams. Under one team, employees' earnings may vary. The board decided that two people with extreme earnings will be released from each such team, i.e. a person earning the most and the person earning the least. Who will survive the reduction and remain employed?

Source: [https://onlinejudge.org/external/117/11727.pdf](https://onlinejudge.org/external/117/11727.pdf)

### Specification

#### Input

* $$a, b, c$$ - three natural numbers determining employee earnings, all in the range $$[1000, 10000]$$

#### Output

* Earnings of an employee who will remain employed

### Example

#### Input

```
a := 1500
b := 1200
c := 1800
```

**Result:** $$1500$$

{% hint style="info" %}
#### Explanation

The smallest value is $$1200$$, and the largest is $$1800$$, so $$1500$$ remains.
{% endhint %}