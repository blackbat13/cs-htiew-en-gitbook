# Blockly

![Comparing numbers - Blockly](<../../../.gitbook/assets/image (9).png>)

## Link to implementation

{% embed url="https://blockly-demo.appspot.com/static/demos/code/index.html?lang=pl#qv4ea5" %}
Comparing numbers - Blockly
{% endembed %}

## Implementation description

At the beginning we read two numbers from the user, providing the messages used and saving them in the variables `a` and `b`.

Then, using the conditional instructions, we check the relationship between loaded values. If the variable values `a` and `b` are equal, we write an equal sign. Otherwise, if the value of the variable `a` is lower than the value of the variable `b`, then we write a sign of minority. Otherwise, we write a sign of the majority.

Note that in the last part of the conditional instructions, we no longer have to check whether the value of the variable `a` is greater than the variable value `b`. This is due to previous conditions. If the variable values are not equal to each other or `a` is not smaller than `b`, we know that `a` is greater than `b`.
