Also known as **Cascading Style Sheets**, CSS is a **styling language** used to control the appearance of HTML elements.

- Defines **colors**, **fonts**, **layouts**, **spacing**, and **responsiveness**.
    
- Makes websites **visually appealing** and **user-friendly**.
    
- CSS is not a programming language—it doesn’t include logic or functions, but it’s essential for front-end development.

---

### There are 3 ways to use CSS

1. **Internal CSS** – Inside the `<style>` tag in an HTML file:

```html
<style>
	h1 { color: blue; }
</style>
```

2. **Inline CSS** – Directly inside an HTML element:

```html
<h1 style="color:blue;">Hi</h1>
```

3. **External CSS** – In a separate `.css` file (recommended for clean structure):

```css
h1 { color: blue; }
```

Then link it in your HTML:

```html
<link rel="stylesheet" href="styles.css">
```

---

### Ways to Apply Styles in CSS

In CSS, you can style HTML elements in three main ways:

- **By tag name** – targets all elements of a specific type.
    
- **By class** – targets multiple elements that share the same class.
    
- **By ID** – targets a single, unique element.

```html
<style>
	h1 { color: blue; }           /* By tag */
	.big { font-size: 40px; }     /* By class */
	#center { text-align: center; } /* By ID */
</style>

<h1>Hi</h1>
<h1 class="big">Hi</h1>
<h1 id="center" class="big">Hi</h1>
```

### Class vs ID: What’s the Difference?

|Feature|`class`|`id`|
|---|---|---|
|Symbol|Starts with a dot (`.`) in CSS|Starts with a hash (`#`) in CSS|
|Usage|Can be reused on multiple elements|Must be unique per page|
|Purpose|For grouping and styling similar elements|For identifying one specific element|
|Example|`<div class="box">`|`<div id="main">`|

#### Use `class` when:

- You want to apply the same style to many elements.
    
- You’re creating reusable components.
    

#### Use `id` when:

- You need to target one specific element.
    
- You’re linking to a section (e.g., with anchor links).
    
- You’re using JavaScript to manipulate a unique element.

---

### Start Styling

#### [[Visual Styling]]

- `Colors`: `color`, `background-color`
    
- `Background`: images, position, size
    
- `Borders`: style, width, color, radius
    
- `Opacity`: transparency
    
- `Box Appearance`: `box-shadow`, `outline`, `filter`
    
#### [[Text Styling]]

- `Text`: alignment, fonts, size, weight, decoration
    
- `Text Effects`: `text-shadow`, `text-transform`, `letter-spacing`, etc.
    

#### [[Box & Layout]]

- `Dimensions`: `width`, `height`, units
    
- `Spacing`: `margin`, `padding`
    
- `Box Model`: explanation and diagram
    
- `Display`: `block`, `inline`, `flex`, etc.
    
- `Flex/Grid Alignment`: `align-items`, `justify-content`, `gap`
    
- `Position`: `relative`, `absolute`, `fixed`, etc.
    
- `Overflow`: `hidden`, `scroll`, etc.
    
- `Visibility`: `visibility`, `display: none`
    
- `Vertical Alignment`: `vertical-align`
    

#### [[Transitions & Effects]]

- `Transitions`: properties, duration, timing
    
- `Hover effects`, `active`, `focus`
    
- Small animations with CSS
    

---
### [[Making CSS Easier]]

CSS can be tricky, especially when building complex layouts. That’s why developers use **CSS frameworks** and **utility libraries** to simplify the process. 

