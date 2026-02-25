In Kotlin there are3 types of loops the `while`, `for` and `do-while` loops

### While

- Used when you **don’t know in advance** how many times the loop should run.
- It continues as long as the condition remains true.

```kotlin
var x = 3
while (x > 0) {
    println("Compte enrere: $x")
    x--
}
```

### For

- Used when you **do know** how many times to repeat, or when you're iterating over a sequence (like a list, string, or range).
- It's great for looping through items.

```kotlin
for (i in 1..5) {
    println("Número: $i")
}
```

### Do While

- Similar to `while`, but it **executes the block at least once** before checking the condition.
- Useful when the loop must run at least one time.

```kotlin
var intent = 1
do {
    println("Intent número: $intent")
    intent++
} while (intent <= 3)
```

---

### Loop modifiers

You can also control the loop direction and range using keywords like `step`, `downTo`, and `until`:

```kotlin
for (i in 1..10 step 2) println(i)       // 1, 3, 5, 7, 9
for (i in 10 downTo 1) println(i)        // 10 to 1 (descending)
for (i in 1 until 5) println(i)          // 1, 2, 3, 4 (excludes 5)
```