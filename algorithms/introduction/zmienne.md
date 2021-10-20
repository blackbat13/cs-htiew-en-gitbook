# Variables

## Admission

What is a variable? You could say that it's a kind of data box. We can perform various types of operations on variables: we can "insert" (**assign**) different values ​​to them, perform operations on them, use them in calculations, and read their values.

Variables are an essential part of practically every algorithm. Therefore, their correct and thorough understanding is required to be able to construct and implement advanced algorithms.

## Types of variables

Imagine two boxes: one plastic and one metal. We can only put fruit in a plastic box, and only nails in a metal box. Each box has its own purpose. The **type** of stored items.

It is similar with the variables. Each variable can only hold a specific type of value. We say then that the variable has its type. For example, we can create a variable to hold integers. We will not assign a value of a different type to such a variable, e.g. text.

{% hint style = "warning"%}
In some programming languages, we explicitly specify the type of a variable when it is created, in others we do not. Similarly, there are languages ​​in which attempting to assign a different type of value to a variable will fail. There are also those in which this type of operation will be allowed. However, that doesn't mean we should do it! It is very important to respect the type of the variables. This is important from the point of view of the readability of the program code, but also from the level of the mechanics behind it.
{% endhint%}

## Variable values

We already know that we can assign values ​​to variables. Does this mean, however, that once assigned a value to a variable remains unchanged? As you can guess from the name **variable**, is not. It is very important to understand that the value of a variable is determined in time, i.e. at a given point in the program operation. To understand this better, let's look at the examples below.

### Example 1

``
1. a := 10
2. Write a
3. a := 2 * a
4. Write a
5. a := a + 5
6. Write a
``

Take a look at the pseudocode above. Can you tell what the values ​​will be printed in statements 2, 4, and 6? Please try to answer this question before proceeding.

The best way is to ** simulate ** the pseudocode. We take a piece of paper and a pen and perform subsequent operations, writing down the values ​​of the variables at each point. This can be done in many ways, one of them is presented below.

``
1. [a = 10]
2. Write 10
3. [a = 2 * 10 = 20]
4. Write 20
5. [a = 20 + 5 = 25]
6. Write 25
``

As you can see, the algorithm presented earlier will enter the following numbers: $$ 10, \ 20, \ 25 $$.

### Example 2

``
1. a := 0
2. Until a < 10, do:
    3. a := a + 2
    4. Write a
``

Again, before continuing, try to think about what successive values ​​the above algorithm will output.

In this example, it is very important to understand how the loop works correctly. The loop repeats certain operations many times, which means that we will execute the same instructions several times. Let's try to write it down.

```
1. [a = 0]

2. While 0 < 10 - OK
    3. [a = 0 + 2 = 2]
    4. Write 2
    
2. While 2 < 10 - OK
    3. [a = 2 + 2 = 4]
    4. Write 4
    
 2. While 4 < 10 - OK
     3. [a = 4 + 2 = 6]
     4. Write 6
     
 2. While 6 < 10 - OK
     3. [a = 6 + 2 = 8]
     4. Write 8
     
 2. While 8 < 10 - OK
     3. [a = 8 + 2 = 10]
     4. Write 10
     
 2. While 10 < 10 - NO (end of the loop)
```