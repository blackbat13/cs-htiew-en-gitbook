# All divisors

## Problem description

{% content-ref url="../../../../algorithms/integers/divisors.md" %}
[divisors.md](../../../../algorithms/integers/divisors.md)
{% endcontent-ref %}

## Trivial solution

### Implementation

```kotlin
fun printDivisors(n: Int) {
  for (i in 1 until n + 1) {
    if (n % i == 0) {
      println(i)
    }
  }
}

fun main() {
  val n = 12

  println("Dzielniki liczby $n:")
  printDivisors(n)
}
```

## Naive solution

### Implementation

```kotlin
fun printDivisors(n: Int) {
  for (i in 1 until (n / 2) + 1) {
    if (n % i == 0) {
      println(i)
    }
  }

  if (n > 1) {
    println(n)
  }
}

fun main() {
  val n = 12

  println("Dzielniki liczby $n:")
  printDivisors(n)
}
```

## Optimal solution

### Implementation

```kotlin
import kotlin.math.sqrt


fun printDivisors(n: Int) {
  for (i in 1 until sqrt(n.toDouble()).toInt() + 1) {
    if (n % i == 0) {
      println(i)

      if (i != n / i) {
        println(n / i)
      }
    }
  }
}

fun main() {
  val n = 12

  println("Dzielniki liczby $n:")
  printDivisors(n)
}
```
