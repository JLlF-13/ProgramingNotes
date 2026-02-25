
### `Text`
Used for single-line plain text input.  

```html
<input type="text" placeholder="Enter your name">
```

---
### `Email`
Validates that the entered text is a valid email address.

```html
<input type="email" placeholder="Enter your email">
```

---
### `Password`
Hides the entered characters (dots or asterisks).

```html
<input type="password" placeholder="Enter your password">
```

---
### `CheckBox`
Allows the user to select one or more options.

```html
<input type="checkbox"> I agree to the terms
```

---
### `Button`
Creates a clickable button.

```html
<input type="button" value="Click Me">
```

---
### `Select`
Dropdown menu for multiple choices.

```html
<select>
  <option>Option 1</option>
  <option>Option 2</option>
</select>
```

---
### `Submit`
Submits the form data.

```html
<input type="submit" value="Send">
```

---
###  `Reset`
Resets all form fields to default values.

```html
<input type="reset" value="Clear">
```

---
### `Radio`
Allows the user to select only one option from a group.

```html
<input type="radio" name="color"> Blue
<input type="radio" name="color"> Red
```

---
### `Number`
Only accepts numeric input.

```html
<input type="number" min="1" max="10">
```

---
### `File` & `Image`
- **File**: lets the user upload a file.
    
- **Image**: submits the form with an image button.  
    

```html
<input type="file">
<input type="image" src="button.png" alt="Submit">
```

---
### `Color`
Opens a color picker.

```html
<input type="color">
```

---
### `Datetime`, `Datetime-local`, `Time` & `Week`
Used for date and time input.

```html
<input type="datetime-local">
<input type="time">
<input type="week">
```

---
### `Hidden`
Stores data that is not visible to the user.

```html
<input type="hidden" value="12345">
```

---
### `Range`
Creates a slider control.

```html
<input type="range" min="0" max="100">
```

---
### `Search`
Similar to text, but optimized for search input.

```html
<input type="search" placeholder="Search...">
```

---
### `Tel`
Accepts phone numbers (no strict validation).

```html
<input type="tel" placeholder="123-456-7890">
```

---
### `Url`
Validates that the input is a valid URL.

```html
<input type="url" placeholder="https://example.com">
```