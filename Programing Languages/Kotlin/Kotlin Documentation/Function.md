## Kotlin functions are declared using the `fun` keyword:

### Normal Function

```kotlin
fun myFunction(fname: String) {
  println(fname + " Doe")
}

fun main() {
  myFunction("John")
  myFunction("Jane")
  myFunction("George")
}
```

Output:

```
// John Doe
// Jane Doe
// George Doe 
```

> The functions can be declared outside of the main or inside

---
### Function with return

```kotlin
fun double(x: Int): Int { 
	return 2 * x 
}
```

---

### Extension functions

This type of functions add something to your program like mathematical formules

```kotlin
fun Int.square(): Int {
	return this * this
}
val myNum = 5
print(myNum.square()) 
```

Output:
```
25
```

---
### Lambda Functions

Betwen `{}` --> {parameters -> lambda body}

```kotlin
val sum = { x: Int, y: Int -> x + y }
print(sum(10,5)) 
```

Output:
```
15
```

#### It

If the lambda has a single parameter, we can use the implicit identifier** `it` **to refer to it within the body of the lambda.

```kotlin
var ints = arrayOf(1,-5,0,2,1,2,-1)
var filteredInts = ints. filter { it > 0 }
print (filteredInts) 
```

Output:
```
[1, 2, 1, 2]
```


#### With return

The value of the last expression is returned. It could also be made explicit:** `return@filter filteredInts`

```kotlin
println(ints.filter {
val filteredInts = it > 0
filteredInts
})
```

Output:
```
[1, 2, 1, 2]
```