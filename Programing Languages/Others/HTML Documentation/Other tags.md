#### `<table>`, `<thead>`, `<tbody>`, `<tr>`, `<td>`, `<th>` 

These tags create structured tables.

```html
<table>
  <thead>
    <tr>
      <th>Name</th>
      <th>Age</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Alice</td>
      <td>30</td>
    </tr>
    <tr>
      <td>Bob</td>
      <td>25</td>
    </tr>
  </tbody>
</table>
```

| Name  | Age |
| ----- | --- |
| Alice | 30  |
| Bob   | 25  |

---

#### `<iframe>`, `<video>`, `<audio>`

These tags embed media content

`<iframe>` – Embed a YouTube video:
```html
<iframe width="300" height="200" src="https://www.youtube.com/embed/dQw4w9WgXcQ" allowfullscreen></iframe>
```

`<video>` – Embed a video file:
```html
<video width="300" controls>
  <source src="video.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>
```

`<audio>` – Embed audio:
```html
<audio controls>
  <source src="audio.mp3" type="audio/mpeg">
  Your browser does not support the audio tag.
</audio>
```


---

#### `<blockquote>`, `<code>`, `<pre>`

`<details>` and `<summary>` – Collapsible content
```html
<details>
  <summary>Click to expand</summary>
  This is hidden content that appears when you click.
</details>
```

`<blockquote>` – Quoted text:
```html
<blockquote>
  "Knowledge is power." – Francis Bacon
</blockquote>
```

`<code>` – Inline code:
```html
Use the <code>print()</code> function to display text.

```

`<pre>` – Preformatted block:
```html
<pre>
Line 1
  Line 2 (indented)
    Line 3 (more indented)
</pre>
```

--- 
#### `<meter>`, `progress` 


`<meter>` – Shows a value within a range:
```html
<meter value="0.6">60%</meter>
```

`<progress>` – Shows task progress:
```html
<progress value="70" max="100">70%</progress>
```