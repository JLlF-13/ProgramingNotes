In Python there are 2 types of loops the `while` and the `for` loops

### While

- Used when you **don’t know in advance** how many times the loop should run.
- It continues as long as the condition remains true.

```python
x = 0
while x < 5:
    print(x)
    x += 1
```

### For

- Used when you **do know** how many times to repeat, or when you're iterating over a sequence (like a list, string, or range).
    
- It's great for looping through items.

```python
for i in range(5):
    print(i)
```