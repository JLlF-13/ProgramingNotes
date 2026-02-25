**Page configuration elements define the behind-the-scenes setup of a webpage.** While semantic tags describe the meaning of visible content, configuration tags like `<title>`, `<meta>`, `<link>`, `<style>`, and `<script>` control how the page behaves, appears, and interacts with browsers and search engines. These elements help define the page’s identity, load external resources, apply styling, and enable dynamic features—making your site faster, smarter, and more discoverable.

---
#### `<title>`
- **Purpose**: Sets the title of the web page.
    
- **Where it appears**: In the browser tab and when bookmarking the page.
    
- **Example**:

```html
<title>My Awesome Website</title>
```

#### `<meta>`
- **Purpose**: Provides metadata about the page (information that’s not displayed directly).
    
- **Common uses**:
    
    - Page description for search engines
        
    - Character encoding
        
    - Viewport settings for responsive design
        
- **Example**:

```html
<meta charset="UTF-8">
<meta name="description" content="A blog about travel and photography.">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

#### `<link>`
- **Purpose**: Connects external resources to the page.
    
- **Common uses**:
    
    - Linking CSS stylesheets
        
    - Adding favicons
        
- **Example**:

```html
<link rel="stylesheet" href="styles.css">
<link rel="icon" href="favicon.ico">
```

#### `<style>`
- **Purpose**: Contains internal CSS rules to style the page.
    
- **Where it goes**: Inside the `<head>` or sometimes in the `<body>` (though not recommended).
    
- **Example**:

```html
<style>
  body {
    background-color: #f0f0f0;
    font-family: Arial, sans-serif;
  }
</style>
```

#### `<script>`
- **Purpose**: Adds JavaScript to the page for interactivity and dynamic behavior.
    
- **Common uses**:
    
    - Form validation
        
    - Animations
        
    - Fetching data
        
- **Example**:

```html
<script>
  alert("Welcome to my site!");
</script>
```

---

Use example:
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="description" content="A simple webpage demonstrating basic HTML structure and page configuration.">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Intro to HTML Page Setup</title>
  <link rel="stylesheet" href="styles.css">
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #f9f9f9;
      padding: 20px;
    }
    h1 {
      color: #333;
    }
    p {
      font-size: 1.1em;
    }
  </style>
  <script>
    console.log("Page loaded successfully!");
  </script>
</head>
<body>
  <h1>Welcome to My HTML Page</h1>
  <p>This page shows how to use basic HTML elements like <code>&lt;title&gt;</code>, <code>&lt;meta&gt;</code>, <code>&lt;link&gt;</code>, <code>&lt;style&gt;</code>, and <code>&lt;script&gt;</code> to configure a webpage.</p>
</body>
</html>
```