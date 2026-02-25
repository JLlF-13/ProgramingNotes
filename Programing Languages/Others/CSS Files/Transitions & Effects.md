CSS transitions and effects allow you to add smooth animations and interactive feedback to your webpage elements. They enhance user experience and make your interface feel more dynamic.

### **Transitions**

Transitions animate changes in CSS properties over time.

```css
transition: property duration timing-function;
```

- **property**: the CSS property to animate (e.g., `background-color`, `transform`, `opacity`)
    
- **duration**: how long the transition lasts (`0.3s`, `1s`, etc.)
    
- **timing-function**: controls the speed curve (`ease`, `linear`, `ease-in`, `ease-out`, `ease-in-out`)

```css
button {
  transition: background-color 0.3s ease;
}

button:hover {
  background-color: #ffcc00;
}
```

### **Hover, Active & Focus Effects**

These pseudo-classes apply styles based on user interaction:

- `:hover` → when the mouse is over the element
    
- `:active` → when the element is being clicked
    
- `:focus` → when the element (like an input) is selected

```css
a:hover {
  color: red;
  text-decoration: underline;
}

button:active {
  transform: scale(0.98);
}

input:focus {
  border-color: blue;
  outline: none;
}
```

### **Small Animations with CSS**

For more advanced animations, use `@keyframes`:

```css
@keyframes fadeIn {
  from { opacity: 0; }
  to { opacity: 1; }
}

.element {
  animation: fadeIn 1s ease-in;
}
```

You can also combine `transform` and `transition` for subtle motion effects:

```css
.card {
  transition: transform 0.3s ease;
}

.card:hover {
  transform: scale(1.05);
}
```

> `@keyframes` is useful for modular page design, allowing you to define reusable animations that can be applied across multiple elements for consistent behavior.