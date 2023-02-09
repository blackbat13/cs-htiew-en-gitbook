# Pseudocode

## Pseudocode

```
1. Read a, b
2. If a = b, then:
    3. Print "="
4. else if a < b, then:
    5. Print "<"
6. else:
    7. Print ">"
```

### Description

At the beginning we load two values from the user (**step 1**). 

Then, using the conditional statement, we check the relationship between the read values. If the values of the variables `a` and `b` are equal to each other (**step 2**) then we print the equal sign (**step 3**). Otherwise, if the value of the variable `a` is less than the value of the variable `b` (**step 4**), then we print the less than sign (**step 5**). Otherwise (**step 6**) we print the greater than sign (**step 7**).

Note that in the last part of the conditional statement (**step 6**), we no longer need to check the value of a variable `a` is greater than the value of the variable `b`. This is due to the previous conditions. If the values of the variables are not equal to each other, neither `a` is not less than `b`, then we know that `a` is greater than `b`.
