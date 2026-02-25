### `if` statement

- Executes a block of code **only if** the condition is true.

```java
int age = 18;
if (age >= 18) {
    System.out.println("You are an adult.");
}
```

### `if-else` statement

- Executes one block if the condition is true, and another if it's false.

```java
int age = 16;
if (age >= 18) {
    System.out.println("You are an adult.");
} else {
    System.out.println("You are a minor.");
}
```

### `else if` statement

- Used to check **multiple conditions** in sequence.

```java
int score = 85;
if (score >= 90) {
    System.out.println("Grade: A");
} else if (score >= 80) {
    System.out.println("Grade: B");
} else if (score >= 70) {
    System.out.println("Grade: C");
} else {
    System.out.println("Grade: F");
}
```

---

### `switch` Statement

- A cleaner way to handle **multiple exact matches** (especially with integers, strings, enums).

```java
int day = 3;
switch (day) {
    case 1:
        System.out.println("Monday");
        break;
    case 2:
        System.out.println("Tuesday");
        break;
    case 3:
        System.out.println("Wednesday");
        break;
    default:
        System.out.println("Unknown day");
}
```