#### A function in bash is made like this:

```bash
say_hi(){}
	echon"Hi"
}
say_hi
```
    

If you wanted to greet someone by name, you could modify the function like this:

```bash
say_hi(){echo "Hi, $1 "}

say_hi "Alice"
say_hi "Bob"
```

Output:

```
Hi, Alice!
Hi, Bob!
```

### What is `$1` in a Bash function?

When you define a function in Bash, you can pass values (called _arguments_) to it. Inside the function, Bash gives you special variables to access those arguments:

- `$1` refers to the **first argument** passed to the function.
    
- `$2` is the **second argument**, and so on.
    
- `$@` represents **all arguments** as a list.