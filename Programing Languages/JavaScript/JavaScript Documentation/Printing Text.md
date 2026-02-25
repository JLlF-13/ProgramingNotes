
We could say that JavaScript has four common ways to display output:

---
### `console.log()`

```javascript
console.log("Hi")
```

- Appears in the browser's console (F12 → Console tab)
    
- Great for developers, invisible to users


---

### `alert()`

```javascript
alert("Hi")
```

- Pops up a message box
    
- Good for quick testing or simple notifications
    
- Interrupts user interaction


---

### `document.write()`

```html
<script>
  document.write("Hello world!");
</script>
```

- Writes directly into the HTML
    
- **Not recommended** — can erase existing content if used after page load


---

### `innerHTML`

```html
<div id="output"></div>

<script>
  document.getElementById("output").innerHTML = "Hello world!";
</script>
```

- Updates part of the page dynamically
    
- Ideal for displaying results, messages, or content changes

