

## What is HTML?

HTML stands for **HyperText Markup Language**.

It is the standard language used to create the **structure** of a
webpage. Every website is built using HTML.

Think of HTML as the skeleton of a website.

-   HTML → Structure
-   CSS → Design
-   JavaScript → Functionality

HTML is **not** a programming language because it cannot make decisions
or perform calculations. It simply tells the browser what should appear
on the webpage.

### Things I Learned

-   HTML is the foundation of every website.
-   Browsers understand HTML tags and display them as webpages.

## What does HyperText Markup Language mean?

### HyperText

HyperText means text that can connect to another webpage using links.

Example:

``` html
<a href="about.html">About Us</a>
```

### Markup

Markup means using tags to describe content.

Example:

``` html
<h1>Welcome</h1>
```

The `<h1>` tag tells the browser this is a heading.

### Language

HTML follows a fixed set of rules that browsers understand.

## Why Do We Use HTML?

If we only write plain text, the browser cannot identify what is a
heading, paragraph, image, or button.

HTML solves this by giving meaning to content.

Example:

``` html
<h1>My Portfolio</h1>
<p>I am learning HTML.</p>
<button>Contact Me</button>
```

The browser now knows how each piece of content should appear.

HTML is commonly used to create:

-   Headings
-   Paragraphs
-   Links
-   Images
-   Tables
-   Lists
-   Forms
-   Buttons
-   Complete webpage layouts

## HTML Editors

An HTML file can be created using any text editor.

Popular editors:

-   Visual Studio Code (VS Code)
-   Notepad
-   Sublime Text
-   Notepad++

I prefer **VS Code** because it provides syntax highlighting,
auto-completion, extensions, Git integration and Live Server support.

## Creating Your First HTML File

Create a folder.

Example:

``` text
MyWebsite
```

Inside it, create a file named:

``` text
index.html
```

The `.html` extension tells the browser it is an HTML file.

`index.html` is usually the first page of a website.

## Basic HTML Structure

``` html
<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <title>My First Page</title>
</head>
<body>

    <h1>Hello World!</h1>
    <p>Welcome to HTML.</p>

</body>
</html>
```

### Understanding Each Part

`<!DOCTYPE html>`

Tells the browser that the document uses HTML5.

`<html>`

The root element. Everything is written inside this tag.

`<head>`

Stores information about the webpage such as the title, CSS files, icons
and meta tags. It is usually not visible on the webpage.

`<body>`

Contains everything the user can actually see, like headings, images,
buttons and paragraphs.

## How Browsers Read HTML

When we open a website:

1.  The browser requests the webpage.
2.  The server sends HTML, CSS and JavaScript files.
3.  The browser reads these files.
4.  The browser converts them into a webpage.

This process is called **rendering**.

## HTML Elements

Everything on a webpage is made using HTML elements.

An element usually has:

-   Opening tag
-   Content
-   Closing tag

Example:

``` html
<p>This is a paragraph.</p>
```

Here,

-   `<p>` → Opening tag
-   `This is a paragraph.` → Content
-   `</p>` → Closing tag

Some elements don't need a closing tag.

Examples:

``` html
<br>
<hr>
<img>
<input>
<meta>
<link>
```

These are called **void (empty) elements**.

## HTML Attributes

After learning elements, I understood that some elements need extra
information.

This extra information is called an **attribute**.

Attributes are written inside the opening tag.

### Syntax

``` html
<tag attribute="value">
```

Example:

``` html
<a href="https://google.com">Google</a>
```

Here,

-   `<a>` creates a link.
-   `href` tells the browser where the link should go.

Another example:

``` html
<img src="cat.jpg" alt="Cute Cat">
```

-   `src` tells the browser which image to display.
-   `alt` shows alternate text if the image cannot be loaded.

Common attributes:

-   id
-   class
-   href
-   src
-   alt
-   style
-   title
-   target

### Things I Learned

-   Attributes provide extra information.
-   Every attribute has a name and a value.
-   Different elements support different attributes.

## Quick Revision

-   HTML creates webpage structure.
-   HTML uses tags to describe content.
-   Browsers render HTML into webpages.
-   Elements are made using tags.
-   Attributes provide extra information.
-   `index.html` is usually the homepage.
-   `head` stores page information.
-   `body` contains visible content.
