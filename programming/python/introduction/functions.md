# Functions

## Introduction

We define the functions in Python, starting with the keyword `def` followed by the name of the function, a list of parameters separated by commas given in round brackets, and then a colon marking the beginning of the function.

### Example

```python
def sum(a, b):
    return a + b
```

## Types suggestions

As with the definitions of variables, in the same way when creating functions we can add suggestion of types for both arguments and returned value.

### Example

```python
def sum(a: int, b: int) -> int:
    return a + b
```

## Procedures

In Python, we do not distinguish procedures from the functions, but of course we can create functions that do not return values.

### Example

```python
def greeting(name: str):
    print(f"Witaj {name}!")
```