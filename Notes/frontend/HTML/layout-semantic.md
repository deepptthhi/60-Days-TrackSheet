

## What is HTML Layout?

After learning basic HTML elements, the next step is arranging them
properly on a webpage. This is called the **layout**.

A good layout makes a website clean, easy to read and easy to maintain.

A common layout looks like this:

-   Header
-   Navigation
-   Main Content
-   Sidebar (optional)
-   Footer

## Semantic HTML

Semantic HTML means using tags that clearly describe their purpose
instead of using only `<div>` everywhere.

Semantic tags improve:

-   Readability
-   Accessibility
-   SEO
-   Code maintenance

Example:

``` html
<header></header>
<nav></nav>
<main></main>
<section></section>
<footer></footer>
```

## Header

`<header>` represents the top section of a webpage.

It usually contains:

-   Logo
-   Website name
-   Navigation
-   Search bar

Example

``` html
<header>
  <h1>My Portfolio</h1>
</header>
```

## Navigation

`<nav>` contains links that help users move between pages.

Example

``` html
<nav>
  <a href="index.html">Home</a>
  <a href="projects.html">Projects</a>
  <a href="contact.html">Contact</a>
</nav>
```

## Main

`<main>` contains the primary content of the webpage.

A page should normally have only one `<main>` element.

Example

``` html
<main>
  <h2>Welcome</h2>
  <p>This is my portfolio.</p>
</main>
```

## Section

`<section>` groups related content together.

Example

``` html
<section>
  <h2>Skills</h2>
  <p>HTML, CSS and JavaScript.</p>
</section>
```

Use it when the content has its own heading.

## Article

`<article>` represents content that can stand on its own.

Examples:

-   Blog post
-   News article
-   Forum post

``` html
<article>
  <h2>Learning HTML</h2>
  <p>Today I learned semantic HTML.</p>
</article>
```

## Aside

`<aside>` contains extra information related to the main content.

Examples:

-   Advertisements
-   Related posts
-   Quick links

``` html
<aside>
  <p>Related Articles</p>
</aside>
```

## Footer

`<footer>` appears at the bottom of a webpage.

It usually contains:

-   Copyright
-   Contact details
-   Social media links
-   Privacy Policy

``` html
<footer>
  <p>© 2026 My Portfolio</p>
</footer>
```

## HTML Iframes

An iframe displays another webpage inside the current webpage.

Syntax

``` html
<iframe src="https://example.com"></iframe>
```

Common uses:

-   Google Maps
-   YouTube videos
-   Embedded websites

## HTML JavaScript

JavaScript adds functionality to HTML.

It can be added using the `<script>` tag.

Example

``` html
<script>
alert("Hello");
</script>
```

Usually JavaScript is kept in a separate file.

``` html
<script src="script.js"></script>
```

## Project Structure

Keeping files organized makes projects easier to manage.

Example

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
└── pages/
```

## Responsive HTML

A responsive webpage adjusts to different screen sizes.

To support mobile devices, include:

``` html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

Responsive design usually works together with CSS media queries.

## HTML Style Guide

Good coding habits make HTML easier to read.

Follow these practices:

-   Use lowercase tag names.
-   Indent code properly.
-   Close tags correctly.
-   Use meaningful class names.
-   Keep folder names simple.
-   Write comments only when necessary.

## Why Semantic HTML Matters

Instead of this:

``` html
<div class="header"></div>
<div class="menu"></div>
<div class="content"></div>
<div class="footer"></div>
```

Use this:

``` html
<header></header>
<nav></nav>
<main></main>
<footer></footer>
```

Anyone reading the code can immediately understand the purpose of each
section.

It also helps search engines and screen readers understand your webpage
better.

## Common Mistakes

-   Using too many `<div>` tags.
-   Having multiple `<main>` elements.
-   Forgetting the viewport meta tag.
-   Using semantic tags only for styling instead of meaning.

## Quick Revision

-   Layout organizes a webpage.
-   Semantic HTML gives meaning to content.
-   `header` is the top section.
-   `nav` stores navigation links.
-   `main` holds the primary content.
-   `section` groups related content.
-   `article` is independent content.
-   `aside` contains extra information.
-   `footer` is the bottom section.
-   `iframe` embeds another webpage.
-   JavaScript adds interactivity.
-   A clean project structure makes development easier.
