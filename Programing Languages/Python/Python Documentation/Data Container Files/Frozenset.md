A **frozenset** is an immutable version of a set. Once created, it cannot be changed. Useful when you need a set to be hashable (e.g., as a dictionary key).

```python
immutable_colors = frozenset(["red", "green", "blue"])
print("green" in immutable_colors)
print("yellow" in immutable_colors)
```

Output: 
True
False