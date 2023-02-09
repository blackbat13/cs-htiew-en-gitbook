# Pseudocode

## Solution

```
1. Read a, b, c
2. sum := a + b + c
3. min := a
4. If b < min, then:
    5. min := b
6. If c < min, then:
    7. min := c
8. max := a
9. If b > max, then:
    10. max := b
11. If c > max, then:
    12. max := c
13. result := sum - min - max
14. Print result
```

### Description

At the beginning we read the input data: three integers (**step 1**).
Then calculate the sum of the numbers loaded (**step 2**).

Now we start finding the smallest value. We use the standard algorithm to find a minimum (**3-7** steps).
Next, we find the maximum in the same way (**steps 8-12**).

Finally, we calculate the result, subtracting the minimum and maximum from the sum and thus leaving the middle value (**step 13**).
We write the calculated result (**step 14**).