In Java there are 3 types of loops the `while`, `for` and `do-while` loops

### While

- Used when you **don’t know in advance** how many times the loop should run.
- It continues as long as the condition remains true.

```java
int i = 0;
while (i < 5) {
    System.out.println("Iteration " + i);
    i++;
}
```

### For

- Used when you **do know** how many times to repeat, or when you're iterating over a sequence (like a list, string, or range).
- It's great for looping through items.

```java
for (int i = 0; i < 5; i++) {
    System.out.println("Iteration " + i);
}
```

### Do while

- Similar to `while`, but it **executes the block at least once** before checking the condition.
- Useful when the loop must run at least one time.

```java
int i = 0;
do {
    System.out.println("Iteration " + i);
    i++;
} while (i < 5);
```

---

### Loop Control Statements

- `break`: exits the loop immediately.
    
- `continue`: skips the current iteration and moves to the next.

#### Break

```java
for (int i = 0; i < 10; i++) {
    if (i == 5) break;
    System.out.println(i);
}
```
#### Continue

```java
for (int i = 0; i < 5; i++) {
    if (i == 2) continue;
    System.out.println(i);
}
```