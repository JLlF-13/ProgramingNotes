### `if` statement

- Executes a block of code **only if** the condition is true.

```csharp
int age = 18;
if (age >= 18) {
    Console.WriteLine("You are an adult.");
}
```

### `if-else` statement

- Executes one block if the condition is true, and another if it's false.

```csharp
int age = 16;
if (age >= 18) {
    Console.WriteLine("You are an adult.");
} else {
	Console.WriteLine("You are a minor.");
}
```

### `else if` statement

- Used to check **multiple conditions** in sequence.

```csharp
int score = 85;
if (score >= 90) {
    Console.WriteLine("Grade: A");
} else if (score >= 80) {
    Console.WriteLine("Grade: B");
} else if (score >= 70) {
    Console.WriteLine("Grade: C");
} else {
    Console.WriteLine("Grade: F");
}
```

---

### `switch` Statement

- A cleaner way to handle **multiple exact matches** (especially with integers, strings, enums).

```java
int day = 3;
switch (day) {
    case 1:
        Console.WriteLine("Monday");
        break;
    case 2:
        Console.WriteLine("Tuesday");
        break;
    case 3:
        Console.WriteLine("Wednesday");
        break;
    default:
        Console.WriteLine("Unknown day");
}