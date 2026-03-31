
### While

#### Normal While

The `while` loop checks the condition before each iteration.

```swift
var attempts = 0
repeat {
  attempts += 1
  print("Attempt #\(attempts)")
} while attempts < 3
```

#### Repeat While

`repeat` runs the body first, then checks the condition.

```swift
var attempts = 0
repeat {
  attempts += 1
  print("Attempt #\(attempts)")
} while attempts < 3
```

---
### For

#### For-in

Use `for-in` to iterate over ranges, arrays, dictionaries, and other sequences.

##### Iterate a Range

Use a range to loop a fixed number of times.

```swift
for i in 1...3 {
  print(i)
}
```

##### Iterate an Array

Loop through an array with `for-in` or `enumerated()` to access index and value.

```swift
let nums = [10, 20, 30]
for n in nums {
  print(n)
}
for (index, value) in nums.enumerated() {
  print("index: \(index), value: \(value)")
}
```

Use `enumerated()` to get index and value together.

#### For-Each

Use `forEach` to iterate sequences with a closure.

#### Iterate with forEach closures

Pass a closure to `forEach` to process each element of a sequence.

```swift
["A","B","C"].forEach { print($0) }
```

#### Enumerated forEach

Use `enumerated()` with `forEach` to get index and value.

```swift
let items = ["A","B","C"]
items.enumerated().forEach { print("\($0.offset): \($0.element)") }
```