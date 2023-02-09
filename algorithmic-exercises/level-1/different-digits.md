# Unique digits

## Description

For a given interval, specify how many numbers in this range consists only of unique digits, i.e. their digits are not repeated.
For example, the number of $$123$$ consists of unique digits, while the number $$100$$ no longer because the digit $$0$$ repeats.

Source: [https://onlinejudge.org/external/125/12527.pdf](https://onlinejudge.org/external/125/12527.pdf)

### Specification

#### Input

* $$a, b$$ - integers from range $$[1,5000]$$

#### Output

* Number of all numbers from range $$[a, b]$$, which consist only of unique digits.

### Example

#### Input

```
87
104
```

#### Output

```
14
```

{% hint style="info" %}
#### Explanation

In the range $$[87,104]$$ the following numbers consists only of unique digits:

$$87,89,90,91,92,93,94,95,96,97,98,102,103,104$$ 
{% endhint %}
