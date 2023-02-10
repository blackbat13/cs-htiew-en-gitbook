# Binary tree

## Problem description

{% content-ref url="../../../../algorithms/fractals/binary-tree.md" %}
[binary-tree.md](../../../../algorithms/fractals/binary-tree.md)
{% endcontent-ref %}

## Implementation

{% code overflow="wrap" lineNumbers="true" %}
```python
import turtle


def binary_tree(rank: int, length: float):
    turtle.forward(length)
    
    if rank > 0:
        turtle.left(45)
        binary_tree(rank - 1, length / 2)
        turtle.right(90)
        binary_tree(rank - 1, length / 2)
        turtle.left(45)
        
    turtle.back(length)


turtle.speed(0)
turtle.penup()
turtle.left(90)
turtle.back(350)
turtle.pendown()
turtle.pensize(3)

binary_tree(5, 400)

turtle.done()
```
{% endcode %}

### Implementation description

Function `binary_tree` (**line 4**) takes two parameters: tree rank and initial branch length. At the beginning, we move the turtle forward by length (**line 5**), in this way drawing a branch. Then, if the rank is larger than zero (**line 7**), it means that we must draw next branches. To this end, we first turn the turtle left by $$45\degree$$ (**line 8**) and by using a recursive call (**line 9**) we draw branches. We do the same with the second branch. First we need to turn the turtle right by $$90\degree$$ (**line 10**), that is $$2*45\degree$$. Then we use recursive call (**line 11**), and then we turn the turtle left by $$45\degree$$ (**line 12**), in this way returning to the initial setting.

Finally, after a possible branching, we move the turtle back by length (**line 14**), thus, returning to the setting from the beginning of calling the function.

In the main code we set the turtle so that the drawn tree fits on the screen (**lines 17-22**). Then we draw a binary tree with our function `binary_tree` (**line 24**), and finally, we finish the turtle actions (**line 26**).