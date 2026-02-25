The `try` block contains code that might throw an exception. If an exception occurs, control jumps to the `catch` block, which handles the error gracefully instead of crashing the program.

```java
try {
    System.out.println("Hi");
} catch (Exception e) {
    System.out.println("An error occurred: " + e.getMessage());
}
```

- `System.out.println` is the correct method.
    
- `catch (Exception e)` declares the type of exception you're catching.
    
- `e.getMessage()` gives a readable error message.

