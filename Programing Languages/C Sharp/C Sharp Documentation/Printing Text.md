
In C#, there are two main ways to print output to the console:

### Option 1: `console.WriteLine()`


```csharp
Console.WriteLine("Hi");
```

Output: 

```
Hi
```

The `WriteLine()` method prints the text and then adds a **line break** (i.e., moves to the next line). Each call to `println` starts on a new line:

```csharp
Console.WriteLine("Hi");
Console.WriteLine("There");
```

Output:

```
Hi
There
```


### Option 2: `console.Write()`

```csharp
console.Write("Hi")
```

Output:

```
Hi
```

Unlike `WriteLine`, the `Write` method **does not** add a line break. So if you use multiple `Write` statements, the output will appear on the same line:

```csharp
console.Write("Hi")
console.Write("There")
```

Output: 

```
Hithere
```
