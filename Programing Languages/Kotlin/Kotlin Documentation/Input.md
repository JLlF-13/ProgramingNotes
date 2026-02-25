In Kotlin, input is read from the console using `readLine()`.

```kotlin
print("What's your name? ")
val name = readLine()
println("Hello, $name")
```

Or in a single line like this:

```kotlin
print("Enter your age: ")
val age = readLine()?.toInt()
```

> `readLine()` returns a nullable `String`, so conversions like `toInt()` should handle possible nulls.

### Other Types of Conversion

|Function|Converts to…|Example usage|
|---|---|---|
|`toInt()`|Integer (`Int`)|`val age = readLine()?.toInt()`|
|`toDouble()`|Decimal (`Double`)|`val price = readLine()?.toDouble()`|
|`toFloat()`|Decimal (`Float`)|`val height = readLine()?.toFloat()`|
|`toLong()`|Large integer (`Long`)|`val population = readLine()?.toLong()`|
|`toBoolean()`|Boolean (`Boolean`)|`val answer = readLine()?.toBoolean()`|
|`toString()`|Text (`String`)|Usually not needed — `readLine()` is already a `String?`|