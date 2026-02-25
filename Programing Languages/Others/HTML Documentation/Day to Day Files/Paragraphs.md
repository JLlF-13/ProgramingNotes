HTML text elements like `<p>`, `<span>`, `<strong>`, and `<em>` help structure and style content. They define how text behaves—whether it's block-level, inline, or semantically meaningful. Mastering them is key to clean, accessible, and well-organized web pages.

---
#### `<p>`

The `<p>` tag defines a paragraph in HTML. It is a block-level element and automatically adds space before and after the content.

```html
<p>This is a paragraph of text.</p>
```

- Use `<p>` to structure readable content.
    
- Avoid nesting block elements (like `<div>`) inside `<p>`.

---

#### `<span>`

The `<span>` tag is an inline container used to style or manipulate small parts of text.

```html
<p>This is a <span style="color: red;">red word</span> in a sentence.</p>
```

- Use `<span>` for styling or scripting small inline portions.
    
- Combine with CSS classes for cleaner code.

---

#### `<strong>` & `<em>`

`<strong>` — Indicates strong importance

```html
<p>This is <strong>very important</strong> information.</p>
```

`<em>` — Indicates emphasis (usually italic)

```html
<p>This is <em>emphasized</em> text.</p>
```

- Use `<strong>` and `<em>` for semantic meaning, not just visual style.
    
- Screen readers recognize these tags for accessibility.