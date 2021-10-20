# Iteration loop

## Simple loop

Sometimes we want to repeat something several times. We don't have any specific condition to fulfill, we just have to repeat an operation many times. We could then write the given operation several times, one after the other, but it is much more convenient to use a loop.

### Example

#### No loops

```
1. Volunteer to the board
2. Volunteer to the board
3. Volunteer to the board
```

#### Using a loop

```
1. Repeat the following 3 times:
    2. Volunteer to the board
```

## Variable number of repetitions

It may also happen that we do not know in advance how many times we will have to repeat a certain operation. Perhaps it depends on other calculations, or maybe it depends on the input data. Then we could not write several repetitions of the given operation one after the other, because we do not know how many would have to be! However, we can do this easily with a loop.

### Example

```
1. Read n
2. Repeat the following n times:
    3. Volunteer to the board
```

## Loop with counter

Sometimes it is not enough for us to repeat a certain operation many times. Sometimes we need something **count** at the same time, e.g. repeating the loop just. Then we need a **loop counter**.

When using a loop with a numerator, we should specify the **range** from which the numerator will take the next values. It's a bit as if we were counting something ourselves, e.g. from $$1$$ to $$5$$. The starting point, i.e. the starting value of the counter, will be $$1$$, and the last value the counter reaches will be $$5$$. In the next **runs** (**iterations**) **of the loop** the counter will take the next values ​​from the set range, so for example the values ​​will be: $$1,2,3,4,5$$.

### Example

#### No loops

```
1. Write on board 1
2. Write on the board 2
3. Write on the board 3
4. Write on the board 4
5. Write on board 5
```

#### Using a loop with a counter

```
1. From i := 1 to 5, do:
    2. Write and on the board
```

#### Block diagram

![Flowchart with loop count] (../../.gitbook/assets/for_ex1.png)

Note that, as with the conditional loop, we also don't have a special block for the iterator loop. In fact, in a block diagram, we execute the iteration loop as a conditional loop, because each iteration loop can be realized with a conditional loop.

## Loop step

The loop step determines how much the value of the loop counter changes with each pass of the loop. The default iteration loop step is $$1$$. If we are using the default value, we usually do not write a loop step. However, we can easily modify it, as the following examples show.

### Example - even numbers

Let's say that our task is to list on the board consecutive even numbers from $$2$$ to $$10$$ inclusive. We could cycle through the values ​​in this range and, if the number is even, write it to the array. We can also modify the loop step so that it goes **only** through consecutive even numbers.

```
1. From i := 2 to 10, with step 2, do:
    2. Write i on the board
```

No loop:

```
1. Write on the board 2
2. Write on the board 4
3. Write on board 6
4. Write on board 8
5. Write on board 10
```

### Example - counting down

What if we want to run from $$5$$ to $$1$$? Here, too, we can use an iterative loop with the appropriate step.

```
1. From i := 5 to 1, with step -1, do:
    2. Write i on the board
```

No loop:

```
1. Write on the board 5
2. Write on the board 4
3. Write on the board 3
4. Write on the board 2
5. Write on board 1
```