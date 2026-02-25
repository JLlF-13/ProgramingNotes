In Python, we mainly work with two categories:

### CONSTANTS
Constants are variables whose values should not change once defined. Python doesn't enforce immutability, but by convention, constants are written in **uppercase**.

```python
NAME = "Joan"  # This is treated as a constant by convention
```
> You can still technically change `NAME`, but it's discouraged in practice.

### VARIABLES
Variables are meant to store data that can change during the execution of the program.

```python
age = 19  # Initial value
age = 20  # Value updated
```

---
### Common Data Types

Python supports several basic types. Here are the four main ones:

#### **String** 
Used for text values

```python
greeting = "Hello world"
```
#### **Integer** 
Used for whole numbers

```python
year = 2077
```
#### **Float** 
Used for decimal numbers, use a dot (`.`) instead of a comma (`,`) to separate decimals

```python
price = 3.141516
```
#### **Boolean** 
Used for logical values

```python
is_active = True
```
>Booleans can only be `True` or `False` (note the capital letters).

--- 

## Don't Forget:

In Python:

- Constants are a naming convention, not a strict rule.
    
- Variables are dynamic and easy to update.
    
- Data types are inferred automatically—you don’t need to declare them explicitly.