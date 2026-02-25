### Basic `if` statement

```python
if x > 0:
    print("Positive")
```

### `if else` statement

```python
if x > 0:
    print("Positive")
else:
    print("Non-positive")
```

### `if elif else` chain

```python
if x > 0:
    print("Positive")
elif x == 0:
    print("Zero")
else:
    print("Negative")
```

---
### Conditional expressions (ternary)

```python
result = "Positive" if x > 0 else "Negative"
```

---
### Truthy and falsy values

Python treats the following as `False` in conditionals:

- `False`, `None`, `0`, `''`, `[]`, `{}`, `set()`
    

Everything else is considered `True`.