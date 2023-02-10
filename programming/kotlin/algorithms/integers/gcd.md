# GCD

## Problem description

{% content-ref url="../../../../algorithms/integers/gcd.md" %}
[gcd.md](../../../../algorithms/integers/gcd.md)
{% endcontent-ref %}

## GCD with subtraction

### Implementation

```kotlin
fun gcd(num1: Int, num2: Int): Int {
  var a = num1
  var b = num2

  while (a != b) {
    if (a > b) {
      a -= b
    } else {
      b -= a
    }
  }

  return a
}

fun main() {
  val a = 32
  val b = 12

  val result = gcd(a, b)

  println("GCD($a, $b) = $result")
}
```

## Iterative GCD with modulo

### Implementation

```kotlin
fun gcd(num1: Int, num2: Int): Int {
  var a = num1
  var b = num2

  while (b != 0) {
    val b2 = b
    b = a % b
    a = b2
  }

  return a
}

fun main() {
  val a = 32
  val b = 12

  val result = gcd(a, b)

  println("GCD($a, $b) = $result")
}
```

## Recursive GCD with modulo

### Implementation

```kotlin
fun gcd(a: Int, b: Int): Int {
  if (b == 0) {
    return a
  }

  return gcd(b, a % b)
}

fun main() {
  val a = 32
  val b = 12

  val result = gcd(a, b)

  println("GCD($a, $b) = $result")
}
```
