Semantic HTML5 elements give meaning to the structure of a webpage. Instead of using generic `<div>` and `<span>` tags everywhere, semantic tags like `<header>`, `<main>`, and `<article>` describe the role of each part of the content. This makes your code easier to read, improves accessibility for screen readers, and boosts SEO performance.

Below you'll find a breakdown of the most important semantic tags, followed by a practical example of how to use them in a simple webpage layout.

---

#### `<header>`
  Defines the top section of a page or content block.  
  Usually contains the logo, title, and introductory elements like navigation or a tagline.

#### `<nav>` 
  Represents a section of navigation links.  
  Used for menus, tables of contents, or any group of internal/external links that help users move around.

#### `<main>`  
  The central content of the document.  
  There should only be one `<main>´ per page, and it excludes headers, footers, and sidebars.

#### `<section>`
  A thematic grouping of content, like a chapter or a part of a page.  
  Often has a heading and can contain articles, images, or other sections.

#### `<article>`
  Self-contained content that could stand alone.  
  Ideal for blog posts, news stories, forum posts, or user comments.

#### `<aside>`  
  Content that is tangentially related to the main content.  
  Think of sidebars, pull quotes, ads, or extra info that complements the main topic.

#### `<footer>` 
  Appears at the bottom of a page or section.  
  Typically includes copyright info, contact links, disclaimers, or related documents.

---

Use example:
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Boring title here</title>
  <style>
    body { font-family: sans-serif; margin: 0; padding: 0; }
    header, nav, main, section, article, aside, footer {
      padding: 1em;
      border-bottom: 1px solid #ccc;
    }
    nav a { margin-right: 10px; }
    aside { background-color: #f9f9f9; }
    footer { text-align: center; font-size: 0.9em; color: #666; }
  </style>
</head>
<body>

  <!-- HEADER: Top section with site title and intro -->
  <header>
    <h1>Welcome to My Website</h1>
    <p>Your daily dose of semantic HTML goodness</p>
  </header>

  <!-- NAV: Navigation menu with links -->
  <nav>
    <a href="#home">Home</a>
    <a href="#articles">Articles</a>
    <a href="#contact">Contact</a>
  </nav>

  <!-- MAIN: Central content of the page -->
  <main>

    <!-- SECTION: Grouping of related articles -->
    <section id="articles">
      <h2>Latest Articles</h2>

      <!-- ARTICLE: Independent content block -->
      <article>
        <h3>Why Semantic HTML Matters</h3>
        <p>Semantic tags help structure your content meaningfully and improve accessibility and SEO.</p>
      </article>

      <!-- ARTICLE: Another standalone content block -->
      <article>
        <h3>Tips for Clean Code</h3>
        <p>Use semantic elements, keep your CSS modular, and comment wisely.</p>
      </article>
    </section>

    <!-- ASIDE: Complementary content, like a sidebar -->
    <aside>
      <h4>Did you know?</h4>
      <p>The <code>&lt;main&gt;</code> tag should only appear once per page!</p>
    </aside>
  </main>

  <!-- FOOTER: Bottom section with legal info -->
  <footer>
    <p>The One Piece is Real</p>
  </footer>

</body>
</html>
```
#### **Tip**: 
Using semantic tags improves accessibility and SEO, and helps screen readers understand the structure of your page better.