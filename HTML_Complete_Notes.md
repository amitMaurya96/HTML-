# Complete HTML Study Notes

## Table of Contents
1. [Introduction to HTML](#introduction-to-html)
2. [HTML Basic Structure](#html-basic-structure)
3. [HTML Tags Overview](#html-tags-overview)
4. [Text Formatting Tags](#text-formatting-tags)
5. [Lists](#lists)
6. [Tables](#tables)
7. [Forms](#forms)
8. [Media Elements](#media-elements)
9. [Semantic Tags](#semantic-tags)
10. [Emmet Shortcuts](#emmet-shortcuts)
11. [SEO and Head Optimization](#seo-and-head-optimization)

---

## Introduction to HTML

### What is HTML?
- **HTML** stands for **Hyper Text Markup Language**
- **Hypertext** - Text with links to other text
- **Markup Language** - Tags that provide structure/meaning to content

### What are Tags?
Tags are markup entities used to:
- Provide structure/meaning to web content
- Add semantic meaning
- Add formatting to content

### Types of Tags:
1. **Semantic Tags** - h1-h6, p, a, ul, ol, table, tr, td, form, input, img, etc.
2. **Structure Tags** - html, head, body, header, main, aside, footer, article, section, nav
3. **Formatting Tags** - b, i, u, strong, em, sup, sub, pre, code, etc.
4. **Non-Semantic Tags** - div (generic wrapper/container)

### Element = Tag (Opening + Closing) + Content

---

## HTML Basic Structure

```
html
<!DOCTYPE html>           <!-- Shows webpage uses HTML5 -->
<html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <meta name="description" content="Description of the webpage">
        <title>Page Title</title>
    </head>
    <body>
        <!-- Content goes here -->
    </body>
</html>
```

### Key Elements:
- `<!DOCTYPE html>` - Declares HTML5 document
- `<html lang="en">` - Root element with language attribute
- `<head>` - Contains metadata
- `<body>` - Contains visible content

---

## HTML Tags Overview

### Headings
Used for titles with priority order (h1 = highest priority, h6 = lowest)
```
html
<h1>Main Heading</h1>
<h2>Sub Heading</h2>
<h3>...</h3>
<h4>...</h4>
<h5>...</h5>
<h6>Lowest Heading</h6>
```

### Paragraph
```
html
<p>Paragraph text goes here.</p>
```

### Anchor (Link)
```
html
<a href="https://example.com">Link Text</a>
<a href="#sectionId">Jump to Section</a>
```

### Preformatted Text
Preserves whitespace and formatting:
```
html
<pre>
    Text as written
    in HTML file
    is preserved
</pre>
```

---

## Text Formatting Tags

| Tag | Description | Example |
|-----|-------------|---------|
| `<b>` | Bold text | **Bold** |
| `<i>` | Italic text | *Italic* |
| `<u>` | Underlined text | Underlined |
| `<strong>` | Important/bold | **Important** |
| `<em>` | Emphasized/italic | *Emphasis* |
| `<sup>` | Superscript | X<sup>2</sup> |
| `<sub>` | Subscript | H<sub>2</sub>O |
| `<mark>` | Highlighted text | Marked |
| `<small>` | Smaller text | Small |
| `<code>` | Code snippet | `code` |
| `<q>` | Quotation | "Quote" |
| `<abbr>` | Abbreviation | HTML |
| `<kbd>` | Keyboard input | Ctrl |

---

## Lists

### Unordered List
```
html
<ul>
    <li>Item 1</li>
    <li>Item 2</li>
    <li>Item 3</li>
</ul>
```

### Ordered List
```
html
<ol>
    <li>First Item</li>
    <li>Second Item</li>
    <li>Third Item</li>
</ol>
```

### Description List
```
html
<dl>
    <dt>Term</dt>
    <dd>Description</dd>
</dl>
```

---

## Tables

### Basic Table Structure
```
html
<table border="1">
    <caption>Table Caption</caption>
    <thead>
        <tr>
            <th>Header 1</th>
            <th>Header 2</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Data 1</td>
            <td>Data 2</td>
        </tr>
    </tbody>
    <tfoot>
        <tr>
            <td>Footer 1</td>
            <td>Footer 2</td>
        </tr>
    </tfoot>
</table>
```

### Table Attributes:
- `colspan` - Number of columns to span
- `rowspan` - Number of rows to span
```
html
<td colspan="2">Spans 2 columns</td>
<td rowspan="3">Spans 3 rows</td>
```

---

## Forms

### Basic Form Structure
```
html
<form action="submit_url" method="POST">
    <!-- Form elements -->
</form>
```

### Form Elements:

#### Label
```
html
<label for="inputId">Label Text</label>
```

#### Input Types
```
html
<!-- Text Input -->
<input type="text" id="name" name="name" placeholder="Enter name">

<!-- Password -->
<input type="password" id="pass" name="password" minlength="6" maxlength="18">

<!-- Email -->
<input type="email" id="email" name="email">

<!-- Phone Number -->
<input type="tel" id="phone" name="phone" pattern="[0-9]{10}">

<!-- Number -->
<input type="number" id="age" name="age" min="18" max="35">

<!-- Date -->
<input type="date" id="dob" name="dob">

<!-- Color -->
<input type="color" id="color" name="color">

<!-- File Upload -->
<input type="file" id="file" name="file" accept=".jpg,.png" multiple>
```

#### Radio Buttons (Select One)
```
html
<fieldset>
    <legend>Select Gender:</legend>
    <input type="radio" id="male" name="gender" value="male">
    <label for="male">Male</label>
    
    <input type="radio" id="female" name="gender" value="female">
    <label for="female">Female</label>
    
    <input type="radio" id="other" name="gender" value="other" checked>
    <label for="other">Other</label>
</fieldset>
```

#### Checkboxes (Select Multiple)
```
html
<fieldset>
    <legend>Select Languages:</legend>
    <input type="checkbox" id="english" name="lang" value="English">
    <label for="english">English</label>
    
    <input type="checkbox" id="hindi" name="lang" value="Hindi">
    <label for="hindi">Hindi</label>
</fieldset>
```

#### Select Dropdown
```
html
<label for="country">Select Country:</label>
<select id="country" name="country" required>
    <option value="" selected>Choose option</option>
    <option value="india">India</option>
    <option value="usa">USA</option>
    <option value="uk">UK</option>
</select>

<!-- Multiple Selection -->
<select id="cars" name="cars" multiple size="2">
    <option value="volvo">Volvo</option>
    <option value="bmw">BMW</option>
</select>
```

#### Textarea
```
html
<label for="message">Message:</label>
<textarea id="message" name="message" rows="5" cols="30" placeholder="Enter message"></textarea>
```

#### Buttons
```
html
<input type="submit" value="Submit">
<input type="button" value="Click Me">
<input type="image" src="button.png" alt="Submit">
<button type="reset">Reset</button>
<button type="button">Button</button>
```

### Input Attributes:
| Attribute | Description |
|-----------|-------------|
| `placeholder` | Hint text |
| `required` | Mandatory field |
| `readonly` | Read-only field |
| `disabled` | Disabled field |
| `min` / `max` | Min/max values |
| `minlength` / `maxlength` | Character limits |
| `pattern` | Regex validation |
| `autocomplete` | Browser autocomplete |
| `inputmode` | Keyboard type (numeric, email, etc.) |

---

## Media Elements

### Image
```
html
<img src="image.jpg" 
     alt="Image description" 
     width="200" 
     height="200" 
     title="Image Title"
     loading="lazy">
```
- `loading="lazy"` - Deferred loading until scroll
- `alt` - Alternative text (important for SEO)
- `title` - Tooltip on hover

### Audio
```
html
<audio controls autoplay loop muted preload="metadata">
    <source src="audio.mp3" type="audio/mpeg">
    Your browser doesn't support audio.
</audio>
```
- `controls` - Play/pause/volume
- `autoplay` - Auto start
- `loop` - Repeat
- `muted` - Start muted
- `preload` - auto/metadata/none

### Video
```html
<video controls width="300" height="200" autoplay loop muted preload="metadata">
    <source src="video.mp4" type="video/mp4">
    Your browser doesn't support video.
</video>
```

### Iframe
```
html
<!-- Embed YouTube -->
<iframe src="https://www.youtube.com/embed/videoId" 
        frameborder="0" 
        allowfullscreen>
</iframe>

<!-- Embed another page -->
<iframe src="page.html" frameborder="0"></iframe>
```

---

## Semantic Tags

Semantic tags clearly describe their meaning to both browser and developer.

### Structure Tags:
| Tag | Description |
|-----|-------------|
| `<header>` | Header section |
| `<nav>` | Navigation links |
| `<main>` | Main content |
| `<section>` | Thematic grouping |
| `<article>` | Self-contained content |
| `<aside>` | Sidebar content |
| `<footer>` | Footer section |
| `<details>` | Collapsible content |
| `<summary>` | Visible heading for details |

### Example:
```
html
<header>
    <h1>Website Title</h1>
    <nav>
        <a href="#home">Home</a>
        <a href="#about">About</a>
    </nav>
</header>

<main>
    <section>
        <article>
            <h2>Article Title</h2>
            <p>Article content...</p>
        </article>
    </section>
    <aside>
        <p>Sidebar content...</p>
    </aside>
</main>

<footer>
    <p>&copy; 2024 Website</p>
</footer>
```

### Details/Summary (Collapsible):
```html
<details>
    <summary>Click to expand</summary>
    <p>Hidden content revealed on click...</p>
</details>
```

---

## Emmet Shortcuts

Emmet is a plugin for faster HTML coding. Use Tab to expand abbreviations.

### Basic Syntax:

| Abbreviation | Output |
|--------------|--------|
| `html:5` | HTML5 boilerplate |
| `head` | `<head>` tag |
| `body` | `<body>` tag |
| `title` | `<title></title>` |
| `link:css` | CSS link |
| `script:src` | JS script |

### Child (>) and Sibling (+):
```
html
<!-- p>div -->
<p>
    <div></div>
</p>

<!-- p+a -->
<p></p>
<a href=""></a>
```

### Multiplication (*):
```
html
<!-- ul>li*3 -->
<ul>
    <li></li>
    <li></li>
    <li></li>
</ul>

<!-- div$*4 -->
<div class="1"></div>
<div class="2"></div>
<div class="3"></div>
<div class="4"></div>
```

### Text Content {}:
```
html
<!-- p{Content} -->
<p>Content</p>

<!-- p>lorem10 (10 words) -->
<p>Lorem ipsum dolor sit amet...</p>
```

### Classes (.) and IDs (#):
```
html
<!-- p.class -->
<p class="class"></p>

<!-- p#id -->
<p id="id"></p>

<!-- .container -->
<div class="container"></div>

<!-- p>span.class -->
<p><span class="class"></span></p>
```

---

## SEO and Head Optimization

### Title Tag
```
html
<title>Page Title | Website Name</title>
```
- Keep under 60 characters
- Include main keywords
- Unique for each page

### Meta Tags

#### Description
```
html
<meta name="description" content="Page description...">
```
- Under 160 characters
- Compelling for click-through

#### Keywords (Deprecated for Google)
```
html
<meta name="keywords" content="html, css, javascript">
```

#### Viewport (Mobile)
```
html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

#### Robots
```
html
<meta name="robots" content="index, follow">
<!-- Options: index/noindex, follow/nofollow -->
```

#### Specific Bots
```
html
<meta name="googlebot" content="index, follow">
<meta name="bingbot" content="index, follow">
```

### Canonical Tag
```
html
<link rel="canonical" href="https://example.com/page">
```

### Open Graph (Facebook/LinkedIn)
```
html
<meta property="og:title" content="Title">
<meta property="og:description" content="Description">
<meta property="og:type" content="website">
<meta property="og:url" content="URL">
<meta property="og:image" content="image.jpg">
```

### Twitter Cards
```
html
<meta name="twitter:card" content="summary_large_image">
<meta name="twitter:title" content="Title">
<meta name="twitter:description" content="Description">
<meta name="twitter:image" content="image.jpg">
```

### Favicon
```
html
<link rel="icon" href="favicon.ico" type="image/x-icon">
```

---

## Block vs Inline Elements

### Block Elements
Start on new line, take full width:
- `div`, `p`, `h1-h6`, `ul`, `ol`, `li`
- `header`, `footer`, `article`, `section`
- `table`, `form`, `pre`, `blockquote`
- `hr`, `canvas`, `noscript`

### Inline Elements
Don't start new line, space = content:
- `span`, `a`, `b`, `i`, `u`
- `strong`, `em`, `mark`, `small`
- `img`, `input`, `button`, `label`
- `select`, `textarea`, `code`

---

## Complete Example

```
html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Learn HTML from basics to advanced">
    <title>HTML Tutorial</title>
    <link rel="icon" href="favicon.ico">
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <header>
        <h1>Welcome to HTML Tutorial</h1>
        <nav>
            <a href="#intro">Introduction</a>
            <a href="#tags">Tags</a>
            <a href="#forms">Forms</a>
        </nav>
    </header>
    
    <main>
        <section id="intro">
            <h2>Introduction</h2>
            <p>HTML is the standard markup language for web pages.</p>
        </section>
        
        <section id="tags">
            <h2>HTML Tags</h2>
            <ul>
                <li>Headings: h1-h6</li>
                <li>Paragraphs: p</li>
                <li>Links: a</li>
                <li>Images: img</li>
            </ul>
        </section>
        
        <section id="forms">
            <h2>Contact Form</h2>
            <form action="/submit" method="POST">
                <label for="name">Name:</label>
                <input type="text" id="name" name="name" required>
                
                <label for="email">Email:</label>
                <input type="email" id="email" name="email" required>
                
                <button type="submit">Submit</button>
            </form>
        </section>
    </main>
    
    <footer>
        <p>&copy; 2024 HTML Tutorial</p>
    </footer>
    
    <script src="script.js"></script>
</body>
</html>
```

---

## Quick Reference

### DOCTYPE Declarations
```
html
<!DOCTYPE html>          <!-- HTML5 -->
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN">  <!-- HTML4 -->
```

### Special Characters
| Character | Code |
|-----------|------|
| & | `&amp;` |
| < | `<` |
| > | `>` |
| " | `"` |
| ' | `&#39;` |
| © | `&copy;` |
| ® | `&reg;` |
| &nbsp; | Non-breaking space |

### Global Attributes
- `id` - Unique identifier
- `class` - CSS class(es)
- `style` - Inline CSS
- `title` - Tooltip text
- `lang` - Language
- `dir` - Text direction (ltr/rtl)
- `data-*` - Custom data attributes

---

## Summary

HTML is the foundation of web development. Key points:
1. **Structure** - Use semantic tags for better SEO and accessibility
2. **Forms** - Master all input types and validation attributes
3. **Media** - Properly implement images, audio, video
4. **SEO** - Optimize head section with proper meta tags
5. **Emmet** - Use abbreviations for faster coding

Happy Learning! 🚀
