# Finding a name

## Problem description

You have a list of names of guests in no particular order. You are given a single name and your task is to determine whether the name is on the list or not.

### Specification

#### Input

* **guests** - list of names in no particular order
* **name** - single string, consists only of lowercase english alphabet letters

#### Output&#x20;

* **YES** if the given name is on the list, **NO** otherwise

### Example 1

#### Input

```
guests := ["bob", "alice", "zebra", "apple"]
name := "zebra"
```

**Output**: YES

### Example 2

#### Input

```
guests := ["bob", "alice", "zebra", "apple"]
name := "pineapple"
```

**Output**: NO

## Exercise 1

Design an algorithm to solve the given problem. Draw a block diagram of that algorithm and implement it in your language of choice.

## Exercise 2

Analyze the effectiveness of your solution. Modify the algorithm to handle many names, i.e. for multiple names check whether they are on the list. How effective is your solution now? Can you think of any way to improve it? If so, draw a block diagram of the new algorithm and implement it in your language of choice.

## Exercise 3

Modify your solution to automatically generate a list of random words, instead of reading them from the input.