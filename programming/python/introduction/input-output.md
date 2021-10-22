---
description: Handling the input and the output
---

# Input / Output

## Output

In order to print something in the console, we use the `print` function.
See the examples below.

### Example 1: simple message

```python
print("Hello World!")
```

### Example 2: more complex message

```python
apple_count = 3
print("I have", apple_count, "apples")
```

### Example 3: formatted message

```python
apple_count = 3
print(f"I have {apple_count} apples")
```

## Input

### Reading in text

```python
name = input("Please enter your name: ")
```

As you can see in the example above, the `input()` function is used to load text from the user. We can pass an optional parameter to the function: the text that will be displayed to the user. As a result, the function returns the entire text line read from the input.

With the `input()` function we can read a line of text from the console. If we want the user to give us a number, we cannot force it, but we can convert the text into a number using the `int()` function.

### Reading in a number

```python
age = int(input("Please input your age: "))
```
