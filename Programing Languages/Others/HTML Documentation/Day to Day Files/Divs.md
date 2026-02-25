A `<div>` is a block-level container element in HTML. It stands for "division" and is used to group together HTML elements. It is commonly used for layout and styling purposes.

```html
<div>
	<h1> I am inside a div</h1>
</div>
```


---

### Why Use `<div>`?

- To organize content into sections.
    
- To apply CSS styles to grouped elements.
    
- To make layouts more manageable and modular.

### Things to Remember

- `<div>` has no semantic meaning by itself.
    
- Use semantic tags like `<section>`, `<article>`, or `<header>` when appropriate.
    
- Overusing `<div>`s can lead to “div soup” — messy and hard-to-maintain code.

## Good Practice

- Use classes or IDs to target specific `<div>`s.
    
- Combine with Flexbox or Grid for layout control.
    
- Keep your HTML clean and readable.


---

### How to center a `<div>`?

```html
<style>
  .centered-div {
    width: 300px;
    margin: 0 auto;
    text-align: center;
    background-color: #f0f0f0;
    padding: 20px;
  }
</style>

<div class="centered-div">
  <h1>I am inside a centered div</h1>
</div>

```