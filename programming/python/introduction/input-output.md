---
description: Obsługa wejścia i wyjścia
---

# Input / Output

## Output

To print a simple message:

```python
print("Hello World!")
```

## Input

### Reading in text

```python
name = input("Please enter your name: ")
```

As you can see in the example above, the `input()` function is used to load text from the user. We can pass an optional parameter to the function: text that will be displayed to the user. As a result, the function returns the entire text line read from the input.

With the `input()` function we can read a line of text from the console. If we want the user to give us a number, we cannot force it, but we can convert the read text into a number using the `int()` function.

### Reading in a number

```python
age = int(input("Please input your age: "))
```
