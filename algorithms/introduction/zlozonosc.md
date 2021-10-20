# Complexity

## Admission

**Complexity** is a very important element in the discussion of algorithms. It is often the key factor by which we compare the **effectiveness** of two solutions / algorithms. We distinguish mainly:

* **time / computational complexity** - i.e. how many operations, depending on the size of the input data, the program has to perform,
* **memory complexity** - how much memory (depending on the size of the input data) the program needs.

In this course, we will not talk about or calculate the exact complexity of algorithms. We will focus on their **estimated pessimistic complexity**.

Therefore, we will not go deep into the mathematical details.

## Big O notation (asymptotic)

We are not going to go into the details of the big $$O$$ asymptotic notation here. In short, we will use it to determine the **pessimistic** time complexity of an algorithm. For example, if the algorithm has the $$O(n)$$ complexity, it means that in the worst case it will act linearly with the data size. Of course, it does not exclude situations in which such an algorithm will work faster.

## Basic complexity classes

| Record           | Name                                    | Example                                |
| ---------------- | --------------------------------------- | -------------------------------------- |
| $$O(1)$$         | constant                                | Checking the triangle condition        |
| $$O(\log{n})$$   | logarithmic                             | Binary Search                          |
| $$O(n) $$        | linear                                  | Linear Search                          |
| $$O(n \log{n})$$ | linearly logarithmic                    | Merge sort                             |
| $$O(n ^ 2)$$     | square                                  | Bubble sort                            |
| $$O(n ^ 3)$$     | cubic                                   | Floyd-Warshall algorithm               |
| $$O(n ^ k)$$     | polynomial ($$k$$ - constant, $$k>1$$)  | -                                      |
| $$O(n!)$$        | n-factorial                             | Listing all permutations of a set      |
| $$O(2^n)$$       | exponential                             | Listing all subsets of the set         |

## Estimating complexity

### Example - linear complexity

``
1. From i := 1 to n, do:
    2. Write i
``

### Example - quadratic complexity

``
1. From i  = 1 to n, do:
    2. From j := 1 to n, do:
        1. Write i * j
``

### Example - cubic complexity

``
1. From i := 1 to n, do:
    2. From j := 1 to n, do:
        3. From k := 1 to n, perform:
            4. Write i * j * k
``

### Example - logarithmic complexity

``
1. As long as n > 0, do:
    2. Write n
    3. n := n div 2
``

{% hint style = "info"%}
**div** means integer division
{% endhint%}

## Cheat sheet

{% embed url = "https://github.com/ro31337/bigoposter/blob/master/bigoposter.pdf"%}