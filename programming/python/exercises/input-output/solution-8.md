# Solution 8

## Exercise

Write a program according to the specification below.

### Specification

#### Input

* $$seconds$$ - natural number

#### Output

* Time given in a legible form $$H:M:S$$ ($$H$$ - hours, $$M$$ - minutes, $$S$$ - seconds)

## Solution

```python
seconds = int(input("Input seconds: "))

hours = seconds // (60 * 60)
    
seconds = seconds % (60 * 60)
    
minutes = seconds // 60
    
seconds = seconds % 60

print(f"{hours}:{minutes}:{seconds}")
```