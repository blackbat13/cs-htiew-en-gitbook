# Coding image

## Description

Computer graphics is very important in computer science.
On computers that store a lot of pictures their effective representation in computer memory is essential.
In this task, we consider the special case of coding an image.
The graphics are presented as rectangular array of capital letters of the English alphabet.
Each letter encodes one region.
Identical regions are encoded by the same letters.

Your task is to count the number of bytes of memory needed for representation the graphics in the computer memory.
The principle is simple: represent the most important region with 2 bytes, and all other regions with a single byte.

**The most important region** is the one that has the most **occurrences**, ie. in the description of graphic the character that represents the region has the highest count.
If several regions have the same largest number of occurrences, we consider all of them to be the most important.


Source: [https://onlinejudge.org/external/115/11588.pdf](https://onlinejudge.org/external/115/11588.pdf)

### Specification

#### Input

* $$h, w$$ - array dimensions, its height and width
* $$pix[h][w]$$ - image description, a two-dimensional array with dimensions $$h\times w$$ in which each element is a capital letter of the English alphabet

#### Output

* The number of bytes needed to represent a given graphic

### Example

#### Input

```
1
5 4
ABCD
ABCA
EFAC
BCAG
AZIP
```

#### Output

```
26
```

{% hint style = "info"%}
#### Explanation

Number of occurrences for each region:
* **A**: 6
* **B**: 3
* **C**: 4
* **D**: 1
* **E**: 1
* **F**: 1
* **G**: 1
* **I**: 1
* **P**: 1
* **Z**: 1

The most common region is the region **A**.
It occurs exactly $$6$$ times.
This means that the region **A** will be encoded with $$2$$ bytes, and all other regions will be encoded with $$1$$ byte.
Hence, we get the following result: $$6*2+14*1=12+14=26$$
{% endhint %}