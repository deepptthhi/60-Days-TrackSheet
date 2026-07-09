

## Basic HTML Structure

``` html
<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Page Title</title>
    <link rel="stylesheet" href="style.css">
</head>

<body>

</body>
</html>
```

## Most Common HTML Tags

  Tag               Purpose
  ----------------- -------------------------
  `<html>`          Root element
  `<head>`          Stores page information
  `<title>`         Browser tab title
  `<body>`          Visible webpage content
  `<h1>` - `<h6>`   Headings
  `<p>`             Paragraph
  `<a>`             Hyperlink
  `<img>`           Display image
  `<br>`            Line break
  `<hr>`            Horizontal line
  `<div>`           Block container
  `<span>`          Inline container
  `<button>`        Button
  `<script>`        JavaScript
  `<link>`          External CSS
  `<style>`         Internal CSS

## Semantic HTML

  Tag           Purpose
  ------------- ---------------------
  `<header>`    Top section
  `<nav>`       Navigation
  `<main>`      Main content
  `<section>`   Related content
  `<article>`   Independent content
  `<aside>`     Side content
  `<footer>`    Bottom section

**Remember:** Semantic tags improve readability, accessibility and SEO.

## Common Attributes

  Attribute       Purpose
  --------------- ----------------------
  `id`            Unique element
  `class`         Reusable styling
  `href`          Link destination
  `src`           Image path
  `alt`           Alternate text
  `title`         Tooltip
  `target`        Open link in new tab
  `style`         Inline CSS
  `placeholder`   Input hint
  `required`      Mandatory input

## Lists

### Unordered List

``` html
<ul>
  <li>HTML</li>
  <li>CSS</li>
</ul>
```

### Ordered List

``` html
<ol>
  <li>Learn HTML</li>
  <li>Learn CSS</li>
</ol>
```

### Description List

``` html
<dl>
  <dt>HTML</dt>
  <dd>Creates webpage structure.</dd>
</dl>
```

## Tables

``` html
<table>
  <tr>
    <th>Name</th>
    <th>Age</th>
  </tr>

  <tr>
    <td>Deepthi</td>
    <td>22</td>
  </tr>
</table>
```

Useful attributes:

-   `colspan`
-   `rowspan`

## Links

``` html
<a href="about.html">About</a>
```

Open in a new tab:

``` html
<a href="https://google.com" target="_blank">
  Google
</a>
```

## Images

``` html
<img src="profile.jpg" alt="Profile Photo">
```

Always use meaningful `alt` text.

## Forms

``` html
<form action="/submit" method="post">

  <label>Name</label>
  <input type="text">

  <button>Submit</button>

</form>
```

### Common Input Types

-   text
-   password
-   email
-   number
-   date
-   checkbox
-   radio
-   file
-   submit

### Useful Input Attributes

-   placeholder
-   required
-   readonly
-   disabled
-   maxlength
-   minlength

## Formatting Tags

  Tag          Meaning
  ------------ -----------------
  `<b>`        Bold
  `<strong>`   Important text
  `<i>`        Italic
  `<em>`       Emphasized text
  `<mark>`     Highlight
  `<small>`    Smaller text
  `<del>`      Deleted text
  `<ins>`      Inserted text
  `<sub>`      Subscript
  `<sup>`      Superscript

## Media

### Audio

``` html
<audio controls>
  <source src="song.mp3">
</audio>
```

### Video

``` html
<video controls>
  <source src="movie.mp4">
</video>
```

### YouTube

``` html
<iframe src="https://www.youtube.com/embed/VIDEO_ID"></iframe>
```

## Graphics

Canvas

``` html
<canvas id="canvas"></canvas>
```

SVG

``` html
<svg width="100" height="100">
  <circle cx="50" cy="50" r="40"/>
</svg>
```

## HTML APIs

-   Geolocation
-   Drag and Drop
-   localStorage
-   sessionStorage
-   Web Workers
-   Server-Sent Events (SSE)

## Project Folder Structure

``` text
project/
│
├── index.html
├── css/
│   └── style.css
├── js/
│   └── script.js
├── assets/
│   ├── images/
│   └── icons/
└── README.md
```

## Best Practices

-   Use semantic HTML.
-   Keep only one `<h1>` per page.
-   Always use `alt` for images.
-   Use lowercase tag names.
-   Keep HTML, CSS and JavaScript separate.
-   Use meaningful class names.
-   Indent code properly.
-   Close tags correctly.
-   Keep folders organized.

## Common Interview Questions

-   What is HTML?
-   HTML vs XHTML?
-   Difference between `id` and `class`?
-   Block vs Inline elements?
-   Why use semantic HTML?
-   What is the purpose of the `<head>` tag?
-   Difference between `<div>` and `<span>`?
-   What is the `alt` attribute?
-   Difference between `localStorage` and `sessionStorage`?
-   What are HTML5 semantic tags?

## Quick Revision

-   HTML = Structure
-   CSS = Design
-   JavaScript = Functionality
-   `<head>` stores page information.
-   `<body>` contains visible content.
-   `id` is unique.
-   `class` is reusable.
-   Semantic HTML improves accessibility and SEO.
-   Forms collect user input.
-   Tables display data.
-   Keep your HTML clean and organized.
