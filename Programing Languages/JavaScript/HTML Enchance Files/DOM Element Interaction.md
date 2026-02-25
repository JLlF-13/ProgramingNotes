## Selecting Elements

#### `getElementById` Explanation

`document.getElementById("id")` selects an HTML element by its unique `id`. Once selected, you can manipulate its style, content, or behavior.

```javascript
let box = document.getElementById("box");
box.style.backgroundColor = "blue";
```

### Other Selection Methods:

|Method|Description|
|---|---|
|`getElementsByClassName()`|Selects all elements with a given class|
|`getElementsByTagName()`|Selects all elements with a given tag|
|`querySelector()`|Selects the first element that matches a CSS selector|
|`querySelectorAll()`|Selects all elements that match a CSS selector|

---

### Mouse Events

These events respond to different mouse actions on elements.

|Event|Description|Example|
|---|---|---|
|`onclick`|Fires when the element is clicked|`element.onclick = () => { ... }`|
|`ondblclick`|Fires when the element is double-clicked|`element.ondblclick = () => { ... }`|
|`onmousedown`|Fires when mouse button is pressed down|`element.onmousedown = () => { ... }`|
|`onmouseup`|Fires when mouse button is released|`element.onmouseup = () => { ... }`|
|`onmouseover`|Fires when mouse enters the element|`element.onmouseover = () => { ... }`|
|`onmouseout`|Fires when mouse leaves the element|`element.onmouseout = () => { ... }`|
|`onmousemove`|Fires when mouse moves over the element|`element.onmousemove = () => { ... }`|

---

###  Click Behavior

Modal Example (Inline HTML)
```html
<button onclick="document.getElementById('modal').style.display='block'">Open modal</button>

<div id="modal" style="display:none;">
  <p>This is a modal!</p>
  <button onclick="document.getElementById('modal').style.display='none'">Close</button>
</div>
```

Modal Example (JavaScript Assignment)
```javascript
document.getElementById("openBtn").onclick = function() {
  document.getElementById("modal").style.display = "block";
};
```

```html
<button id="openBtn">Open modal</button>
```

Remove Click Handler
```javascript
document.getElementById("box").onclick = null;
```

Recommended: `addEventListener`:
```javascript
document.getElementById("box").addEventListener("click", function() {
  this.style.backgroundColor = "green";
});
```

> `addEventListener` allows multiple events and better separation of HTML and JavaScript.