# Conditional statement

## Simple conditional statement

```python
temperature = int(input("Enter the temperature: "))
if temperature < 5:
    print("Cold!")
```

## The expanded conditional statement

```python
temperature = int(input("Enter the temperature: "))
if temperature < 5:
    print("Cold!")
else:
    print("Warmer!")
```

## Full conditional statement

```python
temperature = int(input("Enter the temperature: "))
if temperature < 5:
    print("Cold!")
elif temperature < 20:
    print("Moderate!")
else:
    print("Warm!")
```
