CSS layout properties define how elements are sized, spaced, and positioned on the page. Understanding the box model and layout techniques is key to building responsive and well-structured designs.

### **Dimensions**

Control the size of elements.

```css
width: 200px;
height: 100px;
```

You can use units like:

- `px` → pixels (fixed size)
    
- `%` → percentage of parent
    
- `em`, `rem` → relative to font size
    
- `vh`, `vw` → viewport height/width

### **Spacing**

Defines space inside and around elements.

```css
margin: 20px;   /* space outside the element */
padding: 10px;  /* space inside the element */
```

You can set values for each side:

```css
margin: 10px 20px 15px 5px; /* top, right, bottom, left */
```

or

```css
margin-top: 10px;
margin-right: 20px;
margin-bottom: 15px;
margin-left: 5px;
```

### **Box Model**

Every HTML element is a rectangular box composed of:

- **Content** → text or image
    
- **Padding** → space around content
    
- **Border** → edge around padding
    
- **Margin** → space outside the border
    

> Understanding the box model helps you control spacing and layout precisely.

```css
box-sizing: border-box;
```

This makes `padding` and `border` included in the total `width` and `height`.

### **Display**

Controls how elements behave in the layout.

```css
display: block;     /* takes full width */
display: inline;    /* flows with text */
display: flex;      /* flexible layout */
display: grid;      /* grid layout */
display: inline-block; /* inline flow but allows box dimensions */
```

> `flex` and `grid` are powerful tools for building responsive layouts.

### **Flex/Grid Alignment**

#### Flexbox Layout

A powerful layout model for distributing space and aligning items.

```css
display: flex;
```

Common properties:

- **Direction**:

```css
flex-direction: row;       /* default */
flex-direction: column;
```

- Alignment:

```css
justify-content: center;   /* horizontal alignment */
align-items: center;       /* vertical alignment */
```

- **Gap between items**:

```css
gap: 20px
```

> Flexbox is ideal for one-dimensional layouts (row or column).

#### Grid Layout

Used for two-dimensional layouts (rows and columns).

```css
display: grid;
```

Common properties:

- **Define columns and rows**:

```css
grid-template-columns: 1fr 2fr;
grid-template-rows: auto 100px;
```

- Spacing

```css
gap: 10px;
```

- Item placement

```css
justify-items: center;
align-items: start;
```

>Grid gives you precise control over complex layouts.

### **Position**

Defines how elements are placed on the page.

```css
position: static;    /* default */
position: relative;  /* offset from normal position */
position: absolute;  /* positioned relative to nearest ancestor */
position: fixed;     /* stays in place on scroll */
```

Use `top`, `right`, `bottom`, `left` to adjust placement.

### **Overflow**

Controls what happens when content exceeds its container.

```css
overflow: hidden;   /* cuts off overflow */
overflow: scroll;   /* adds scrollbars */
overflow: auto;     /* scrollbars if needed */
```

### **Visibility**

Controls whether an element is visible.

```css
visibility: visible; /* default state */
visibility: hidden;     /* hides but keeps space */
display: none;          /* removes from layout */
```

> Use `display: none` to completely remove an element from the page flow.

### **Vertical Alignment**

Used to align inline or inline-block elements vertically.

```css
vertical-align: top;
vertical-align: middle;
vertical-align: bottom;
```

> Only works with inline-level elements or table cells. For block elements, use Flexbox or Grid.