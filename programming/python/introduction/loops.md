# Loops

## Iterative loop

An iterator loop in Python is actually a loop that traverses a range of values. It can be a list, a collection, and others. Using the range function, we can create a range of successive values and go through it. Note that the range function simulates in a sense a right-open range.

Below are some examples of the classic Python iterator loop construction.

#### Print the numbers from **0** to **9** **inclusive**

```python
for i in range(10):
    print(i)
```

#### Print the numbers from **1** to **9** **inclusive**

```python
for i in range(1, 10):
    print(i)
```

#### Print every second value from **0** to **8** **inclusive**

```python
for i in range(0, 10, 2):
    print(i)
```

#### Print the numbers from **10** to **1** **inclusive**

```python
for i in range(10, 0, -1):
    print(i)
```

## Conditional loop

A conditional loop in Python looks like it does in many other languages. Here is a simple example.

#### Print the numbers from **0** to **9** **inclusive**

```python
i = 0
while i < 10:
    print(i)
    i += 1
```

Note the use of the `+=` operator on line 4. This is intentional, because Python 3 does not have the `++` operator.
