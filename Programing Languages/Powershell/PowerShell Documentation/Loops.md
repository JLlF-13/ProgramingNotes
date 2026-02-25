
In Powershell there are 4 types of loops the `while`, `for`, `do...while` and `foreach` 

### While

- Used when you **don’t know in advance** how many times the loop should run.
- Continues as long as the condition is true.

```powershell
$i = 1
while ($i -lt 6) {
  Write-Output $i
  $i++
}
```

### For

- Used when you **do know** how many times to repeat.
- Ideal for iterating over ranges or sequences.

```powershell
for ($x = 0; $x -le 10; $x++) {
  Write-Output "The number is: $x"
}
```

### Do...While

- Similar to `while`, but the condition is **checked after** the loop runs.
- Ensures the loop runs **at least once**.

```powershell
$i = 1
do {
  Write-Output $i
  $i++
} while ($i -lt 6)
```

### Foreach

- Used to **iterate over collections** like arrays or lists.
- Automatically loops through each element.

```powershell
$colors = @("red", "green", "blue")

foreach ($color in $colors) {
  Write-Output $color
}
```

You can also access both **key** and **value** in hashtables:

```powershell
$person = @{name = "Anna"; age = 28}

foreach ($key in $person.Keys) {
  Write-Output "$key: $($person[$key])"
}
```