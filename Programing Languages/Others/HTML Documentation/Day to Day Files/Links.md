**Links** (also called **hyperlinks**) are used to navigate between pages on the same website or to external websites. In HTML, they are created using the `<a>` tag.

### Basic Structure
```html
<a href="url">Text</a>
```
- `href`: Specifies the destination URL.
    
- The text between the tags is what users click on.

### The `target` Attribute

The `target` attribute defines **where** the linked document will open. Here are the most common values:

| Value     | Description                                                             |
| --------- | ----------------------------------------------------------------------- |
| `_self`   | Default. Opens the link in the **same tab or window**.                  |
| `_blank`  | Opens the link in a **new tab or window**.                              |
| `_parent` | Opens the link in the **parent frame** (used with frames).              |
| `_top`    | Opens the link in the **full body of the window**, removing any frames. |

Example Using `target="_blank"`
```html
<a href="url" target="_blank">Text</a>
```
This link will open the destination in a new tab.