### Simple comment

```python
print("Hi!")
#print("How are you?")
print("Bye!")
```

This is the standard way to comment out a single line in Python using `#`. It's clean, clear, and widely used.
### Multi-line "Comment" Using Strings

Option1:
```python
print("Hi!")
"""
How
are
you?
"""
print("Bye!")
```

Option2:
```python
print("Hi!")
'''
How
are
you?
'''
print("Bye!")
```

These technically work, but they’re not true comments. Python treats them as **multi-line strings** that aren’t assigned to any variable, so they’re ignored at runtime. However, they still exist in memory and can be misleading.