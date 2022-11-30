# Python

## Implementation

```python
a = int(input("Podaj a: "))
b = int(input("Podaj b: "))

if a == b:
    print("=")
elif a < b:
    print("<")
else:
    print(">")
```

### Link to implementation

{% embed url="https://ideone.com/xRH1Ti" %}
Comparing two numbers - Python
{% endembed %}

### Implementation description

At the beginning we read two values ​​from the user (**lines 1 and 2**). Since we expect integers, in addition to the `input` function, we also use the `int` function to convert loaded values ​​(which are stored in the form of a `string` characters) into integers.

Then, using the conditional instructions, we check the relationship between the loaded values. If the values of the variables ​​`a` and `b` are equal (**line 4**), we write an equal sign (**line 5**). Otherwise, if the value of the variable `a` is lower than the value of the variable `b` (**line 6**), then we write a minority sign (**line 7**). Otherwise (**line 8**) we write the sign of the majority (**line 9**).

Note that in the last part of the conditional instructions (**line 8**), we no longer need to check whether the value of the variable `a` is greater than the value of the variable `b`. This is due to previous conditions. If the variable values ​​are not equal to each other and `a` is not smaller than `b`, we know that `a` is greater than `b`.
