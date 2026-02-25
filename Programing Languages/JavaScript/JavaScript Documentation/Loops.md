JavaScript has up to 6 types of loops. We'll divide them into **commonly used** and **not so commonly used** based on how frequently they're used in everyday coding.


---

## Comonly used

### While

- Used when you **don’t know in advance** how many times the loop should run.
- It continues as long as the condition remains true.

```javascript
let i = 0;
while (i < 5) {
  console.log(i);
  i++;
}
```

### For

- Used when you **do know** how many times to repeat, or when you're iterating over a sequence (like a list, string, or range).
- It's great for looping through items.

```javascript
for (let i = 0; i < 5; i++) {
  console.log(i);
}
```

### Foreach

- A method used to loop through **arrays**.
- It executes a provided function once for each array element.

```javascript
const fruits = ["apple", "banana", "cherry"];
fruits.forEach(function(fruit) {
  console.log(fruit);
});
```

### Do while

- Similar to `while`, but it **executes the block at least once** before checking the condition.
- Useful when the loop must run at least one time.

```javascript
let i = 0;
do {
  console.log(i);
  i++;
} while (i < 5);
```


---

## Not comonly used

### for...in

- Used to iterate over the **enumerable properties of an object**.
- Best suited for objects, not arrays (can give unexpected results with arrays).

```javascript
const person = { name: "Alice", age: 25 };
for (let key in person) {
  console.log(key + ": " + person[key]);
}
```

### for...of

- Used to iterate over **iterable objects** like arrays, strings, maps, sets, etc.
- Provides direct access to the **values** rather than the keys or indices.

```javascript
const colors = ["red", "green", "blue"];
for (let color of colors) {
  console.log(color);
}
```