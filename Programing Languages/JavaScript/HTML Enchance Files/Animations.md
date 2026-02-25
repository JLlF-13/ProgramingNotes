Animations in JavaScript allow you to create dynamic visual effects by changing styles over time. You can use inline styles, CSS classes, or JavaScript transitions.

---
### Simple Animation with `onclick`

```html
<div id="box" style="width:100px; height:100px; background:red;"></div>

<script>
  document.getElementById("box").onclick = function() {
    this.style.transition = "transform 0.5s";
    this.style.transform = "scale(1.2)";
  };
</script>
```
This scales the box when clicked, using a smooth transition.

---
### Toggle Animation with CSS Class

```html
<style>
  .grow {
    transform: scale(1.2);
    transition: transform 0.5s;
  }
</style>

<div id="box" style="width:100px; height:100px; background:red;"></div>

<script>
  document.getElementById("box").onclick = function() {
    this.classList.toggle("grow");
  };
</script>
```

Using `classList.toggle()` lets you apply and remove the animation repeatedly.

---

### Animate Multiple Properties

```javascript
element.style.transition = "all 0.5s";
element.style.opacity = "0.5";
element.style.transform = "rotate(15deg)";
```

You can animate multiple style properties at once using `"all"` or listing them individually.

---
### Delay and Timing Functions

You can control animation timing with CSS:

```css
transition: transform 0.5s ease-in-out;
```

Or use `setTimeout()` in JavaScript for delayed effects:

```javascript
setTimeout(() => {
  element.style.transform = "scale(1.5)";
}, 1000); // 1 second delay
```