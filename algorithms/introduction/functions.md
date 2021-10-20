# Functions

## Introduction

Imagine a black magic box. Such a box into which we throw something and something else falls out of it. We put **input** into it, and we get the **output**:

![](<../../.gitbook/assets/image (32).png>)

In other words, we put some **data** in a box and extract **the result** from it:

![](<../../.gitbook/assets/image (33).png>)

Such a box represents a **function**.

## What is a function?

In programming, we can understand the concept of a function in many ways. It's easiest to think of it as some **part** of a program that has a specific task and its own name. We pass data to the function in the form of **parameters**, and in response we get the result consistent with the **specification** of the function.

{% hint style="danger" %}
Do not confuse functions in programming and functions in mathematics, they are two completely different creations!
{% endhint %}

The schematic notation of the function is as follows:

```
function FunctionName(parameter1, parameter2, ...):
    Operation1
    Operation2
    ...
    Return result
```

## Example - a coffee machine

Imagine a coffee machine like it stands in the corridors of many offices, schools and train stations. We can say that it represents a function according to the following specification:

### Specification

#### Data

* **selection** - selected drink
* **money** - amount due

#### Result

* Selected drink.

{% hint style="info" %}
Obviously, this is a very simplified specification. In fact, such a vending machine will not give us a drink unless we pay the appropriate fee. Sometimes, in addition to a drink, we also get the rest. However, this specification is enough for an example.
{% endhint %}

Let's try to write a fragment of a function performed by such an automaton in the form of a pseudocode:

```
function AutomaticCoffeeMachine(selection, money):
     1. If selection = "latte" and money = 3.0, then:
         2. Return the Latte and exit
```

## Procedure

Contrary to the function, procedure **does not return a specific result**. So what could its purpose be? The procedure can be used to, for example, change the values of variables passed as parameters (if we pass them properly), change the values of global variables, or print a message on the screen. We can easily imagine a greeting procedure that takes the user's first name and displays an appropriate message on the screen:

``
procedure Greeting(name):
     1. Write "Hello"
     2. Write name
     3. Write "!"
     4. Write a newline character
     5. Finish
``

{% hint style = "warning"%}
Nowadays, we practically do not distinguish between function and procedure. In many programming languages, there are only functions, including those that do not return a result (or the result of which we ignore).
{% endhint%}