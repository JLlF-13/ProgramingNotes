
## Declaring a Variable

Kotlin uses two keywords to declare variables:

| Keyword | Mutability                | Example             |
| ------- | ------------------------- | ------------------- |
| `val`   | Immutable (cannot change) | `val name = "Joan"` |
| `var`   | Mutable (can change)      | `var age = 25`      |
- Use `val` when the value shouldn't change, and `var` when it might.

### Type Inference

Kotlin can **automatically detect** the type based on the assigned value:

```kotlin
val city = "Barcelona"      // String
var score = 90              // Int
val isSunny = true          // Boolean
```

You can also **explicitly specify** the type:

```kotlin
val country: String = "Spain"
var temperature: Double = 22.5
```

### Common Data Types

| Type      | Description      | Example             |
| --------- | ---------------- | ------------------- |
| `Int`     | Integer numbers  | `val x = 42`        |
| `Double`  | Decimal numbers  | `val pi = 3.14`     |
| `Boolean` | True or false    | `val isOpen = true` |
| `String`  | Text             | `val name = "Leo"`  |
| `Char`    | Single character | `val grade = 'A'`   |
### Nullability

Kotlin forces you to handle `null` safely:

```kotlin
var email: String? = null  // Nullable type
email = "user@example.com"
```

Use the `?` to allow a variable to hold `null`.