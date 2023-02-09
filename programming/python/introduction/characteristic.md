# Language-specific statements

There are some statements in Python that are not found in other programming languages, at least not in that form. Here we will try to provide just such instructions.

## Arithmetic instructions

### The exponentiation operator `**`

```python
two_to_ten = 2 ** 10 # 1024
```

### Integer division operator `//`

```python
five_by_two = 5 // 2 # 2
```

## Creating lists

In Python, new lists are empty by default. We can fill them with initial values, but we cannot give them an initial size. The statement `list = [10]` means to create a list with one element: the number 10, not a list of size 10, as you might think from C ++.

However, there is a way to create a list of a certain size: by filling it with initial values. We can of course do this in a loop, but Python gives us a simpler construct for creating lists: **list comprehension**.

### Create a ten-element zero-filled list

```python
lst = [0 for _ in range(10)]
```

### Create a ten-element list filled with consecutive values from 0 to 9, inclusive

```python
lst = [i for i in range(10)]
```

### Create a list from text

```python
text = "a b c d e f"
lst = text.split(" ") # ["a", "b", "c", "d", "e", "f"]
```
