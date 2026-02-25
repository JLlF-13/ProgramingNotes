
In Java, **functions** are called **methods**. They are blocks of code that perform a specific task and can be reused throughout your program.

## Defining a Method

```java
returnType methodName(parameters) {
    // code to execute
}
```

Example:

```java
public static void say_hi() {
    System.out.println("Hello!");
}
```

> This method is called `say_hi`, returns nothing (`void`), and prints a message.

### Calling a Method

To use a method, you **call** it by its name followed by parentheses:

```java
say_hi() // Output: Hello!
```

### Methods with Parameters

You can pass values into methods using **parameters**.

```java
public static void greetUser(String name) {
    System.out.println("Hello, " + name + "!");
}
```

Calling it:

```java
greetUser("Rashford"); // Output: Hello, Alice!
```

### Methods that Return Values

Some methods return a result using the `return` keyword.

```java
public static int add(int a, int b) {
    return a + b;
}
```

Calling it:

```java
int result = add(3, 4); // result is 7
```