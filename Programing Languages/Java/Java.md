
[[Programing Languages/Java/Java Documentation/Printing Text|Printing Text]]
[[Programing Languages/Java/Java Documentation/Variables & Types|Variables & Types]]
[[Programing Languages/Java/Java Documentation/Conditional|Conditional]]
[[Programing Languages/Java/Java Documentation/Loops|Loops]]
Data Conatiners
[[Programing Languages/Java/Java Documentation/Functions|Functions]]
[[Programing Languages/Java/Java Documentation/Comments|Comments]]
[[Try...Catch]]
[[Imports & Packages]]

---
### Java Rule: File Name Must Match Public Class Name

One of Java’s key rules is that **the filename must match the name of the public class it contains**. This ensures clarity and consistency in how Java programs are organized and compiled.

#####  Why is this important?

- Java uses the public class name to generate the corresponding `.class` file during compilation.
    
- If the filename doesn’t match the public class name, the compiler will throw an error.
    
- This rule helps maintain a clean structure, especially in large projects with many classes.

```java
// File: HelloWorld.java
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, world!");
    }
}
```

✅ In this example, the file is named `HelloWorld.java`, which matches the public class `HelloWorld`.

❌ If the file were named `Greeting.java`, the compiler would show an error like: `class HelloWorld is public, should be declared in a file named HelloWorld.java`

> Also, if the file contains a public class but **does not include a** `main` **method**, and you try to run it directly, the compiler will not throw an error — but the program **won’t execute anything**, because Java won’t know where to start.

---

## What Does `public` Mean in Java?

In Java, `public` is an **access modifier**. It defines **who can use or see** a class, method, or variable.

### Meaning of `public`

- When something is marked as `public`, it means it is **accessible from anywhere** — from any other class, even in other packages.
    
- It’s like saying: “This is open to the whole program.”

Example: Public Class

```java
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, world!");
    }
}
```

- `public class HelloWorld`: This class can be accessed from other classes.
    
- Because it's `public`, the **file name must be** `HelloWorld.java`.

Example: Public Method

```java
public static void greet() {
    System.out.println("Hi!");
}
```

- This method `greet()` is `public`, so it can be called from anywhere in your program.


---

### Other Access Modifiers

|Modifier|Access Level|
|---|---|
|`public`|Accessible from any class|
|`private`|Accessible only within the same class|
|`protected`|Accessible within the same package or subclasses|
|_(default)_|Accessible only within the same package (no keyword used)|
> The same rules apply to methods, variables, and inner classes.