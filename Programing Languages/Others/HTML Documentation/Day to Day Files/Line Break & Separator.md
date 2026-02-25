### Line Break (`<br>`)

The `<br>` tag creates a **line break** inside a block of text. It’s an empty tag, meaning it doesn’t need a closing tag.

```html
<p>This is one line.<br>This is another line.</p>
```

Use it when you want manual control over line breaks—like in poems, addresses, or formatted text.

---
### Horizontal Separator (`<hr>`)

The `<hr>` tag inserts a **horizontal line** across the page, often used to visually separate sections of content.

```html
<h2>Section 1</h2>
<p>Content of section 1</p>
<hr>
<h2>Section 2</h2>
<p>Content of section 2</p>
```

By default, it’s a thin gray line. You can style it with CSS:
```html
<hr style="border: none; height: 2px; background-color: #333;">
```

---

### Pro Tips

- Avoid using `<br>` for layout spacing—use CSS (`margin`, `padding`) instead.
    
- `<hr>` can be used semantically to indicate a thematic break or shift in content.
