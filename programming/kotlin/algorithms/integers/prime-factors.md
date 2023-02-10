# Prime factors

## Problem description

{% content-ref url="../../../../algorithms/integers/prime-factors.md" %}
[prime-factors.md](../../../../algorithms/integers/prime-factors.md)
{% endcontent-ref %}

## Implementation

```kotlin
fun distribute(num: Int): List<Int> {
  var primeFactors: MutableList<Int> = mutableListOf()
  var i = 2
  var n = num

  while (n > 1) {
    if (n % i == 0) {
      primeFactors.add(i)
      n /= i
    } else {
      i++
    }
  }

  return primeFactors
}

fun main() {
  val n = 124

  val result = distribute(n)

  println("Prime factors of $n: $result")
}
```
