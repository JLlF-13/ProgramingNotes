#### A function in Powershell is made like this:

```powershell
function Say-Hi{
	Write-Output "Hi"
}
Say-Hi
```



If you wanted to greet someone by name, you could modify the function like this:

```powershell
function Say-Hi {
    param($name)
    Write-Output "Hi, $name!"
}

Say-Hi "Alice"
Say-Hi "Bob"
```

Output:

```
Hi, Alice!
Hi, Bob!
```

This version accepts a **parameter** (`name`) and uses it to personalize the greeting. Functions like this are the building blocks of larger programs.

> Functions like this are the building blocks of larger scripts. You can add logic, loops, conditionals, and even return values.