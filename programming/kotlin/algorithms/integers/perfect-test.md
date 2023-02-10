# Perfect test

## Problem description

{% content-ref url="../../../../algorithms/integers/perfect-test.md" %}
[perfect-test.md](../../../../algorithms/integers/perfect-test.md)
{% endcontent-ref %}

## Implementation

```kotlin
fun isPerfect(n: Int): Boolean {
  var sum = 0

  for (i in 1 until n) {
    if (n % i == 0) {
      sum += i
    }
  }

  return sum == n
}

fun main() {
  val n = 6

  val result = isPerfect(n)

  if (result) {
    println("$n is perfect")
  } else {
    println("$n is not perfect")
  }
}
```
