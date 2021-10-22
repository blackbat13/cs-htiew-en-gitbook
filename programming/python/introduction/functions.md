# Functions

In Python functions begin with a `def` keyword, followed by the function name and list of parameters listed inside brackets.
As practically every block in Python a function begins with a colon.

The general scheme of the function looks as follows:

```
def function_name(list_of_parameters):
    function_body
```

## Example: a function that returns the sum of two values

```python
def sum(a, b):
    return a + b
```

## Example: a function that returns the sum of two values with type suggestions added

Usually it's a good idea to add type suggestions to the function definition.
It will not affect the execution of the program, but may help understand better what is going on and what was the intended format of the function.

```python
def sum(a: int, b: int) -> int:
    return a + b
```
