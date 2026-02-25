
### `if` statement

- Executes a block of code **only if** the condition is true.

```kotlin
int age = 18;
if (age >= 18) {
    println("You are an adult.");
}
```

### `if-else` statement

- Executes one block if the condition is true, and another if it's false.

```kotlin
int age = 16;
if (age >= 18) {
    println("You are an adult.");
} else {
    println("You are a minor.");
}
```

### `else if` statement

- Used to check **multiple conditions** in sequence.

```kotlin
int score = 85;
if (score >= 90) {
    println("Grade: A");
} else if (score >= 80) {
    println("Grade: B");
} else if (score >= 70) {
    println("Grade: C");
} else {
    println("Grade: F");
}
```

> In Kotlin, the `if` statement can be used as an expression to assign a value to a variable. It returns a result based on the condition.

```kotlin
val temperature = 12

val weatherDescription = if (temperature < 0) {
    "Freezing cold"
} else if (temperature in 0..15) {
    "Chilly"
} else if (temperature in 16..25) {
    "Mild"
} else {
    "Hot"
}

println("Today's weather: $weatherDescription")
```

---

### when Statement

- A cleaner way to handle **multiple exact matches** (especially with integers, strings, enums), very similar to `switch` in other languiages

```kotlin
val day = 3
val nameDay = when (day) {
	1 -> "Monday"
	2 -> "Tuesday"
	3 -> "Wednesday"
	4 -> "Thursday"
	5 -> "Friday"
	6, 7 -> "Weekend"
	else -> "Invalid day"
}
println(nameDay)
```

---

### Conditional expressions (ternary)

```kotlin
val age = 18
val message = if (age >= 18) "Adult" else "Minor"
println(message)
```