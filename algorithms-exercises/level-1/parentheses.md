# Parentheses

## Description

You are given a string of parentheses () and [].
Your goal is to check whether the string is **correct** or not.
A string of this type is said to be **correct** when:
* it is the empty string,
* if $$A$$ and $$B$$ are correct, then $$AB$$ is also correct,
* if $$A$$ is correct, then $$(A)$$ and $$[A]$$ are also correct.


Source: [https://onlinejudge.org/external/6/673.pdf](https://onlinejudge.org/external/6/673.pdf)

### Specification

#### Input

* $$par$$ - string of parentheses

#### Output

* Message saying whether the given string is correct or not

### Example 1

#### Input

```
([])
```

#### Output

```
Correct
```

### Example 2

#### Input

```
(([()])))
```

#### Output

```
Not correct
```

### Example 3

#### Input

```
([()[]()])()
```

#### Output

```
Correct
```