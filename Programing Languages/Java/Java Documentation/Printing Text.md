
In Java, there are two main ways to print output to the console:

### Option 1: `System.out.println()`

```java
System.out.println("Hi")
```

Output: 

```
Hi
```

The `println` method prints the text and then adds a **line break** (i.e., moves to the next line). Each call to `println` starts on a new line:

```java
System.out.println("Hi")
System.out.println("There")
```

Output:

```
Hi
There
```


### Option 2: `System.out.print()`

```java
System.out.print("Hi")
```

Output:

```
Hi
```

Unlike `println`, the `print` method **does not** add a line break. So if you use multiple `print` statements, the output will appear on the same line:

```java
System.out.print("Hi")
System.out.print("There")
```

Output: 

```
Hithere
```
