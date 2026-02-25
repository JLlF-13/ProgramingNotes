
### `onkeydown`, `onkeyup` 

Keyboard events allow you to detect and respond when the user presses keys. There are three main types:

|Event|Description|
|---|---|
|`keydown`|Fires when a key is pressed down|
|`keyup`|Fires when a key is released|
|`keypress`|_(Deprecated)_ Used to fire when a key is pressed, but now replaced by `keydown`|

> Use_ `keydown` _for most interactions._ `keypress` _is outdated and not recommended._

---

### Example: Detecting Key Press

```html
<input type="text" id="inputBox" placeholder="Type something..." />

<script>
  document.getElementById("inputBox").addEventListener("keydown", function(event) {
    console.log("Key pressed:", event.key);
  });
</script>
```

This logs the key the user presses while typing in the input box.

### Example: Trigger Action with Specific Key

```javascript
document.addEventListener("keydown", function(event) {
  if (event.key === "Enter") {
    alert("You pressed Enter!");
  }
});
```

You can use `event.key` to check for specific keys like `"Enter"`, `"Escape"`, `"ArrowUp"`, etc.

---

### Common `event.key` Values

|Key|Value|
|---|---|
|Enter|`"Enter"`|
|Escape|`"Escape"`|
|Space|`" "`|
|Arrow Up|`"ArrowUp"`|
|Arrow Down|`"ArrowDown"`|
|a-z|`"a"` to `"z"`|
|0-9|`"0"` to `"9"`|

---

### Prevent Default Behavior

Sometimes you want to stop the browser’s default action (like submitting a form when Enter is pressed):

```javascript
document.addEventListener("keydown", function(event) {
  if (event.key === "Enter") {
    event.preventDefault();
  }
});
```

> It can be useful in case you want to check a form before sending it to the server.