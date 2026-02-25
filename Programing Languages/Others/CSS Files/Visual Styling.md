## Colors

CSS comes with a set of default color names like `red`, `blue`, and `green`, but it also supports more advanced formats such as `RGB`, `HEX`, `HSL`, and `CSS Variables`. This gives you flexibility to create consistent and visually appealing designs.

#### Color

Used to change the color of text.

```html
<h1 style="color:blue;">This text is color blue</h1>
```

You can also use RGB or HEX codes:

```html
<p style="color:rgb(255, 0, 0);">This text is red</p>
<p style="color:#00ff00;">This text is green</p>
```

#### Background color

Used to change the background color of an element.

```html
<div style="background-color:lightgray;">
    <p>This background is light gray</p>
</div>
```

You can also add transparency using RGBA:

```html
<div style="background-color:rgba(0, 0, 255, 0.5);">
    <p>Blue background with 50% opacity</p>
</div>
```

#### Gradients

Gradients allow smooth transitions between colors.

- Linear Gradiant

```css
background: linear-gradient(to right, red, yellow);
```

- Radiant Gradiant

```css
background: radial-gradient(circle, red, yellow);
```

You can customize direction, shape, and color stops to create stunning effects.

#### Variable CSS

CSS variables help maintain consistency across your styles by defining reusable values.

```css
:root {
  --primary-color: #3498db;
  --secondary-color: #2ecc71;
}

h1 {
  color: var(--primary-color);
}

button {
  background-color: var(--secondary-color);
}
```

By changing the variable in `:root`, you update the style everywhere it's used.

---

## Background

The `background` property in CSS allows you to style the area behind an element. You can use solid colors, images, gradients, and more.

#### Background Color

Sets a solid color as the background.

```html
<div style="background-color:lightblue;">
  <p>This background is light blue</p>
</div>
```

#### Background Image

Adds an image as the background.

```css
background-image: url('image.jpg');
```

You can combine it with other properties:

- `background-repeat`: `repeat`, `no-repeat`, `repeat-x`, `repeat-y`
    
- `background-position`: `center`, `top left`, `bottom right`, etc.
    
- `background-size`: `cover`, `contain`, or specific values
    
- `background-attachment`: `scroll` or `fixed` (for parallax effect)

```css
background: url('image.jpg') no-repeat center center;
background-size: cover;
```

#### Gradient Backgrounds

Use gradients for smooth transitions between colors.

```css
background: linear-gradient(to right, #ff7e5f, #feb47b);
background: radial-gradient(circle, #ff7e5f, #feb47b);
```

---

## Borders

Borders define the edges of an element and can be styled in various ways.

#### Border Style

```css
border-style: solid; /* Options: dashed, dotted, double, groove, etc. */
```

#### Border Width

```css
border-width: 2px;
```

#### Border Color

```css
border-color: #333;
```

### Border Radius

Rounds the corners of an element.

```css
border-radius: 10px;
```

You can combine all in shorthand:

```css
border: 2px dashed red;
```

### Outline vs Border

`outline` is similar to `border` but doesn't affect layout and can be used for focus styles.

```css
outline: 2px solid blue;
```


---

## Opacity

Opacity controls the transparency of an element.

#### Basic Usage

```css
opacity: 0.5; /* 0 = fully transparent, 1 = fully opaque */
```

This affects the entire element, including its children.

#### Using RGBA for Partial Transparency

Instead of changing the whole element’s opacity, you can use RGBA to apply transparency to colors only.

```css
background-color: rgba(255, 0, 0, 0.3); /* Red with 30% opacity */
```

---

### **Box Appearance**

These properties enhance the visual style of boxes and containers.

- **Border Radius**: rounds the corners

```css
border-radius: 10px;
```

- **Box Shadow**: adds depth with shadows

```css
box-shadow: 2px 2px 8px rgba(0, 0, 0, 0.3);
```

- **Outline**: adds a line outside the border (doesn’t affect layout)

```css
outline: 2px solid blue;
```

- **Filter**: applies visual effects like blur or brightness

```css
filter: blur(4px);
filter: brightness(1.2);
```

> These effects help create visual hierarchy and focus.