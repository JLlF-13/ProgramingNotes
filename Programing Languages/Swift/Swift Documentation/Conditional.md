### Basic `if` statement

```swift
if x > 0 {
    print("Positive")
}
```

### `if else` statement

```swift
if x > 0 {
    print("Positive")
} else {
    print("Non-positive")
}
```

### `if elif else` chain

```swift
if x > 0 {
    print("Positive")
} else if x == 0 {
    print("Zero")
} else {
    print("Negative")
}
```

---
### Conditional expressions (ternary)

```swift
let age = 20
let status = (age >= 18) ? "Adult" : "Minor"
```

---

###  `Switch` statement

Match integer ranges and exact values.

Add `default` to handle remaining cases.

```swift
let grade = 82
switch grade {
case 90...100:
  print("A")
case 80..<90:
  print("B")
case 70..<80:
  print("C")
default:
  print("Below C")
}
```