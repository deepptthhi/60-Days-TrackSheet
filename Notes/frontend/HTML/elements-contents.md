

## HTML Headings

### What are Headings?

Headings are used to give titles and subtitles to a webpage. They help
users understand the content and also improve SEO.

HTML provides six heading tags from `<h1>` to `<h6>`.

`<h1>` is the most important heading and `<h6>` is the smallest.

### Syntax

``` html
<h1>Main Heading</h1>
<h2>Sub Heading</h2>
```

### Example

``` html
<h1>My Portfolio</h1>
<h2>Projects</h2>
<h3>Skills</h3>
```

### Things I Learned

-   Use only one `<h1>` on a page.
-   Don't use headings just to increase font size.

## HTML Paragraphs

Paragraphs are used to display normal text.

### Syntax

``` html
<p>Your text here</p>
```

### Example

``` html
<p>I am learning HTML and building webpages.</p>
```

The browser automatically leaves some space before and after each
paragraph.

## HTML Formatting

Formatting tags make text easier to read and highlight important
information.

Common tags:

-   `<b>` → Bold
-   `<strong>` → Important text
-   `<i>` → Italic
-   `<em>` → Emphasized text
-   `<mark>` → Highlight
-   `<small>` → Smaller text
-   `<del>` → Deleted text
-   `<ins>` → Inserted text
-   `<sub>` → Subscript
-   `<sup>` → Superscript

### Example

``` html
<p>This is <strong>important</strong>.</p>
<p>Water = H<sub>2</sub>O</p>
<p>2<sup>3</sup> = 8</p>
```

## HTML Quotations

Quotation tags are used when showing quotes or references.

Common tags:

-   `<blockquote>` → Long quote
-   `<q>` → Short quote
-   `<abbr>` → Abbreviation
-   `<cite>` → Title of a book, movie, etc.
-   `<address>` → Contact information

### Example

``` html
<q>Practice makes perfect.</q>
```

## HTML Links

Links connect one page to another.

The `<a>` tag is called the anchor tag.

### Syntax

``` html
<a href="URL">Link Text</a>
```

### Example

``` html
<a href="about.html">About</a>
```

Here `href` tells the browser where to navigate.

Useful attributes:

-   href
-   target
-   download
-   title

Use `target="_blank"` to open a link in a new tab.

## HTML Images

Images are displayed using the `<img>` tag.

It is a void element, so it does not need a closing tag.

### Syntax

``` html
<img src="image.jpg" alt="Description">
```

### Example

``` html
<img src="profile.jpg" alt="Profile Photo">
```

-   `src` → image location
-   `alt` → text shown if the image cannot load

Always provide meaningful `alt` text for accessibility.

## HTML Lists

Lists help organize information.

### Unordered List

``` html
<ul>
  <li>HTML</li>
  <li>CSS</li>
</ul>
```

Shows bullet points.

### Ordered List

``` html
<ol>
  <li>Learn HTML</li>
  <li>Learn CSS</li>
</ol>
```

Shows numbered items.

### Description List

``` html
<dl>
  <dt>HTML</dt>
  <dd>Creates webpage structure.</dd>
</dl>
```

## HTML Tables

Tables display data in rows and columns.

Important tags:

-   `<table>`
-   `<tr>` → Table Row
-   `<th>` → Table Heading
-   `<td>` → Table Data

### Example

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

-   colspan
-   rowspan

## Block and Inline Elements

### Block Elements

Block elements start on a new line and take the full width available.

Examples:

-   div
-   p
-   h1
-   section
-   article

### Inline Elements

Inline elements stay on the same line and only take the required width.

Examples:

-   span
-   a
-   img
-   strong
-   em

## HTML Div

`<div>` is a block-level container.

It is mainly used to group related elements together so they can be
styled or controlled easily.

### Example

``` html
<div class="card">
    <h2>Title</h2>
    <p>Content</p>
</div>
```

## HTML Span

`<span>` is an inline container.

It is mostly used to style a small part of text.

### Example

``` html
<p>Hello <span style="color:red;">World</span></p>
```

## HTML Class

A class is used when multiple elements need the same style.

### Example

``` html
<p class="info">Welcome</p>
<p class="info">Hello</p>
```

Many elements can share one class.

## HTML Id

An id uniquely identifies one element.

Only one element should use a particular id.

### Example

``` html
<h1 id="title">Portfolio</h1>
```

IDs are commonly used with CSS and JavaScript.

## HTML Buttons

Buttons allow users to perform actions.

### Syntax

``` html
<button>Click Me</button>
```

### Example

``` html
<button>Submit</button>
```

Buttons can later be connected to JavaScript.

## HTML Computer Code Elements

HTML provides special tags for displaying code.

Important tags:

-   `<code>` → Code
-   `<pre>` → Preserves spaces and line breaks
-   `<kbd>` → Keyboard input
-   `<samp>` → Program output
-   `<var>` → Variable

### Example

``` html
<pre>
print("Hello")
</pre>
```

`<pre>` keeps the formatting exactly as written.

## Common Mistakes

-   Using headings only for size instead of hierarchy.
-   Forgetting the `alt` attribute on images.
-   Using many `<br>` tags for spacing.
-   Using `id` where a `class` is more appropriate.
-   Using tables for webpage layout instead of displaying tabular data.

## Quick Revision

-   Headings organize content.
-   Paragraphs display text.
-   Formatting tags improve readability.
-   Links connect pages.
-   Images use `src` and `alt`.
-   Lists organize information.
-   Tables display data.
-   Block elements start on a new line.
-   Inline elements stay on the same line.
-   `div` groups elements.
-   `span` styles small text.
-   `class` is reusable.
-   `id` is unique.
-   Buttons perform actions.
-   Code tags display programming code clearly.
