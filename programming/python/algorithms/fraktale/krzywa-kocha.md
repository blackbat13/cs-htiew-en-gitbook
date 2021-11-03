# Krzywa Kocha

## Problem description

{% content-ref url="../../../../algorithms/fraktale/krzywa-kocha.md" %}
[krzywa-kocha.md](../../../../algorithms/fraktale/krzywa-kocha.md)
{% endcontent-ref %}

## Implementation

```python
import turtle


def koch_curve(rank, length):
    if rank > 0:
        koch_curve(rank - 1, length / 2)
        turtle.left(60)
        koch_curve(rank - 1, length / 2)
        turtle.right(120)
        koch_curve(rank - 1, length / 2)
        turtle.left(60)
        koch_curve(rank - 1, length / 2)
    else:
        turtle.forward(length)


turtle.speed(0)
turtle.penup()
turtle.back(350)
turtle.pendown()

koch_curve(3, 200)

turtle.done()
```

### Link do implementacji

{% embed url="https://replit.com/@damiankurpiewski/Koch-Curve#main.py" %}

### Implementation descriptioni

TODO
