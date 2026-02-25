
In Java, **variables** are used to store data, and each variable must have a **type** that defines what kind of data it can hold. Java is a **statically typed language**, which means you must declare the type of a variable when you create it.

## Declaring a Variable

```java
type name = value;
```

#### Common Data Types

| Description | Example                         | Example                  |
| ----------- | ------------------------------- | ------------------------ |
| `int`       | Integer numbers                 | `int x = 10;`            |
| `double`    | Decimal numbers                 | `double pi = 3.14;`      |
| `boolean`   | True or false values            | `boolean isOpen = true;` |
| `char`      | A single character              | `char grade = 'A';`      |
| `String`    | A sequence of characters (text) | `String name = "Bob";`   |
#### Type Conversion

Java allows **type casting** between compatible types.

```java
int x = 10;
double y = x; // automatic conversion (int → double)
```

For manual conversion:

```java
double a = 9.8;
int b = (int) a; // manual cast (double → int)
```

> “Take the value of `a`, cut off the decimal part, and store it in `b`.”

is describing a **manual type conversion** — also known as **casting** — where you're **converting a variable**