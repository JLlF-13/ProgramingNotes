Forms in HTML are used to collect user input, like text, selections, or files. They’re essential for things like login pages, surveys, and contact forms.

### Create a form

Start by creating a `<form>` tag. Inside this tag, you can include labels, inputs, buttons, and other elements to capture user data.

- Always use `<label>` for accessibility and clarity
    
- Use `name` attributes to identify each input field
    
- Validate input with HTML attributes or JavaScript for better user experience

#### Basic Example

```html
<form action="/submit" method="post">
  <label for="name">Name:</label>
  <input type="text" id="name" name="name">

  <input type="submit" value="Send">
</form>
```

---

### [[Input types]]

There are different types of `<input>` elements in HTML, each designed to collect specific kinds of user data.

Some common types include:

- `text` — for plain single-line input
    
- `email` — for email addresses (includes basic validation)
    
- `password` — hides the input characters
    
- `checkbox` — allows binary choices (checked/unchecked)
    
- `select` — creates a dropdown menu (technically not an `<input>`, but often used in forms)