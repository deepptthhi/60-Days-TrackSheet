

## What are HTML APIs?

An API (Application Programming Interface) allows a webpage to use
features provided by the browser.

Instead of building everything from scratch, HTML and JavaScript can use
browser APIs to access useful features like location, storage, drag and
drop, and background processing.

## Geolocation API

The Geolocation API allows a website to get the user's current location
(with permission).

Common uses:

-   Maps
-   Food delivery
-   Ride booking
-   Weather apps

Example:

``` javascript
navigator.geolocation.getCurrentPosition(showPosition);
```

The browser always asks the user for permission before sharing the
location.

## Drag and Drop API

This API allows users to drag an element and drop it somewhere else.

Common uses:

-   Moving cards
-   Uploading files
-   Reordering tasks

Important events:

-   dragstart
-   dragover
-   drop

## Web Storage

Web Storage allows websites to save data inside the browser.

There are two types.

### localStorage

Data remains even after the browser is closed.

Example:

``` javascript
localStorage.setItem("name","Deepthi");
```

### sessionStorage

Data exists only until the browser tab is closed.

Example:

``` javascript
sessionStorage.setItem("theme","dark");
```

Use localStorage for user preferences and sessionStorage for temporary
data.

## Web Workers

Normally JavaScript runs on a single thread.

A Web Worker allows heavy tasks to run in the background without
freezing the webpage.

Common uses:

-   Large calculations
-   Data processing
-   File conversion

## Server-Sent Events (SSE)

SSE allows the server to continuously send updates to the browser
without refreshing the page.

Common uses:

-   Live scores
-   Stock prices
-   News feeds
-   Notifications

## Accessibility

Accessibility means making websites usable for everyone, including
people with disabilities.

Good practices:

-   Use semantic HTML.
-   Add meaningful alt text to images.
-   Use labels with form fields.
-   Maintain proper heading order.
-   Make buttons easy to understand.

Accessibility improves user experience and is considered a good
development practice.

## SEO Basics

SEO stands for Search Engine Optimization.

Good HTML helps search engines understand a webpage.

Basic SEO tips:

-   Use one `<h1>` tag.
-   Add meaningful page titles.
-   Write descriptive alt text.
-   Use semantic HTML.
-   Keep URLs simple.

## Folder Organization

Keeping projects organized makes development easier.

Example:

``` text
project/
│
├── index.html
├── css/
├── js/
├── assets/
│   ├── images/
│   ├── icons/
│   └── videos/
├── pages/
└── README.md
```

## HTML Best Practices

While learning HTML, I found these habits make code cleaner and easier
to maintain.

-   Use semantic HTML instead of many divs.
-   Write meaningful class names.
-   Indent code properly.
-   Close tags correctly.
-   Use lowercase tag names.
-   Separate HTML, CSS and JavaScript files.
-   Add comments only when necessary.
-   Keep files organized.

## Common Mistakes

-   Forgetting the `alt` attribute.
-   Using inline CSS everywhere.
-   Using tables for layout.
-   Skipping heading levels.
-   Using many `<br>` tags for spacing.
-   Giving multiple elements the same `id`.

## Interview Tips

-   Know the difference between `id` and `class`.
-   Understand semantic HTML.
-   Know when to use `localStorage` and `sessionStorage`.
-   Be able to explain accessibility and SEO.
-   Understand the purpose of common form elements.

## HTML Quick Cheat Sheet

### Basic Structure

``` html
<!DOCTYPE html>
<html>
<head>
</head>
<body>
</body>
</html>
```

### Most Used Tags

-   html
-   head
-   body
-   h1 to h6
-   p
-   a
-   img
-   div
-   span
-   ul
-   ol
-   li
-   table
-   form
-   input
-   button
-   header
-   nav
-   main
-   section
-   article
-   footer

## Final Revision

-   HTML creates webpage structure.
-   Semantic HTML improves readability, accessibility and SEO.
-   Forms collect user input.
-   Tables display data.
-   CSS styles HTML.
-   JavaScript adds functionality.
-   Web Storage saves browser data.
-   Web Workers run background tasks.
-   Geolocation gets the user's location.
-   Clean, semantic and organized HTML is easier to maintain.
