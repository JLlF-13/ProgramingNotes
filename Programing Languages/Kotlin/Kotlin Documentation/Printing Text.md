
In Kotlin, there are two main ways to print output to the console:

### Option 1: `println()`

```kotlin
println("Hi")
```

Output: 

```
Hi
```

The `println` method prints the text and then adds a **line break** (i.e., moves to the next line). Each call to `println` starts on a new line:

```kotlin
println("Hi")
println("There")
```

Output:

```
Hi
There
```

### Option 2: `print()`

```kotlin
print("Hi")
```

Output:

```
Hi
```

Unlike `println`, the `print` method **does not** add a line break. So if you use multiple `print` statements, the output will appear on the same line:

```kotlin
print("Hi")
print("There")
```

Output: 

```
Hithere
```
