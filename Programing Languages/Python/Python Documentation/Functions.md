#### A function in Python is made like this:

```python
def SayHi():
	print("Hi")
SayHi()
```


If you wanted to greet someone by name, you could modify the function like this:

```python
def Say_hi(name):
    print(f"Hi, {name}!")

Say_hi("Alice")
Say_hi("Bob")
```

Output:

```
Hi, Alice!
Hi, Bob!
```

This version accepts a **parameter** (`name`) and uses it to personalize the greeting. Functions like this are the building blocks of larger programs.