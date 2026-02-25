Images are added to web pages using the `<img>` tag. This tag is **self-closing**, meaning it doesn’t require a closing tag.

### Basic Structure

```html
<img src="image-url" alt="Description of the image">
```
- `src`: Specifies the path or URL of the image.
    
- `alt`: Provides alternative text shown if the image fails to load. It’s also important for accessibility and SEO.

### Useful Attributes
| Attribute | Description                                                            |
| --------- | ---------------------------------------------------------------------- |
| `width`   | Sets the width of the image (in pixels or percentage).                 |
| `height`  | Sets the height of the image.                                          |
| `title`   | Displays a tooltip when the user hovers over the image.                |
| `loading` | Controls how the image loads: `lazy` (delayed) or `eager` (immediate). |
Example with Multiple Attributes
```html
<img src="img.jpg" alt="Some img" width="300" height="200" title="Magic Image" loading="lazy">
```
This example shows an image with defined dimensions, a descriptive alt text, a tooltip, and lazy loading for better performance.