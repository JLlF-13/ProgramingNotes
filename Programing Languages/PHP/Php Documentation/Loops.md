
In PHP there are 4 types of loops the `while`, the `for`, the `do...while` and the `foreach` loops

### While

- Used when you **don’t know in advance** how many times the loop should run.
- It continues as long as the condition remains true.

```php
$i = 1;
while ($i < 6) {
  echo $i;
  $i++;
}
```

### For

- Used when you **do know** how many times to repeat, or when you're iterating over a sequence (like a list, string, or range).
- It's great for looping through items.

```php
for ($x = 0; $x <= 10; $x++) {
  echo "The number is: $x <br>";
}
```

### Do...While

- Similar to `while`, but the condition is **checked after** the loop runs. 
- This means the loop will **always execute at least once**, even if the condition is false.

```php
$i = 1;
do {
  echo $i;
  $i++;
} while ($i < 6);
```

### Foreach

- Used specifically to **iterate over arrays**.
- It loops through each element without needing a counter.

```php
$colors = array("red", "green", "blue");

foreach ($colors as $color) {
  echo "$color <br>";
}
```

You can also access both **key** and **value**:

```php
$person = array("name" => "Anna", "age" => 28);

foreach ($person as $key => $value) {
  echo "$key: $value <br>";
}
```