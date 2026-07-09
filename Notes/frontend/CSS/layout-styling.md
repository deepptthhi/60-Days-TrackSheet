

## CSS Display

One thing I noticed while learning CSS is that every HTML element behaves differently. Some elements take the full width of the page, while others only take the space they need. The **display** property controls this behavior.

### Why do we use display?

* To control how elements appear on the page.
* To arrange elements properly.
* To create different layouts.

### Syntax

```css
selector {
    display: value;
}
```

### Common Display Values

### block

A block element always starts on a new line and takes the full available width.

Examples:

* `<div>`
* `<h1>`
* `<p>`

```css
div {
    display: block;
}
```

### inline

An inline element only takes as much width as it needs.

Examples:

* `<span>`
* `<a>`
* `<strong>`

```css
span {
    display: inline;
}
```

### inline-block

It behaves like an inline element but allows us to set width and height.

```css
button {
    display: inline-block;
}
```

### none

This completely hides an element.

```css
p {
    display: none;
}
```

The element won't be visible and won't take up any space.

## CSS Max-width

Earlier, I used the `width` property for everything. Later, I learned that **max-width** is often a better choice because it makes websites more responsive.

### Why do we use max-width?

It prevents an element from becoming wider than a certain size.

### Syntax

```css
max-width: 800px;
```

### Example

```css
.container {
    width: 100%;
    max-width: 800px;
}
```

If the screen is smaller than 800px, the container shrinks automatically.

This is why `max-width` is commonly used in modern websites.

## CSS Position

The **position** property decides where an element appears on the page.

### Syntax

```css
position: value;
```

### static

This is the default position.

The element appears normally in the document.

```css
position: static;
```

### relative

The element stays in its original place, but we can move it slightly using top, bottom, left, or right.

```css
position: relative;
```

### absolute

The element is positioned relative to its nearest positioned parent.

```css
position: absolute;
```

### fixed

The element stays in the same place even when the page is scrolled.

This is commonly used for navigation bars.

```css
position: fixed;
```

### sticky

The element behaves normally until it reaches a certain position while scrolling. Then it sticks to that position.

```css
position: sticky;
top: 0;
```

Sticky headers are a common example.

## CSS Position Offsets

After using `position`, we can move elements using offset properties.

### top

```css
top: 20px;
```

Moves the element down.

### bottom

```css
bottom: 20px;
```

Moves the element upward from the bottom.

### left

```css
left: 30px;
```

Moves the element to the right.

### right

```css
right: 20px;
```

Moves the element toward the left.

Example:

```css
.box {
    position: relative;
    top: 20px;
    left: 40px;
}
```

## CSS Z-index

Sometimes two elements overlap each other.

The **z-index** property decides which element appears on top.

### Syntax

```css
z-index: 1;
```

Example

```css
.box1 {
    position: absolute;
    z-index: 2;
}

.box2 {
    position: absolute;
    z-index: 1;
}
```

Since **box1** has a higher value, it appears above **box2**.

Remember:

`z-index` works only on positioned elements.

## CSS Overflow

Sometimes the content inside a box becomes too large.

The **overflow** property controls what should happen in that situation.

### visible

Default value.

Content simply comes out of the box.

```css
overflow: visible;
```

### hidden

Extra content is hidden.

```css
overflow: hidden;
```

### scroll

Scrollbars are always shown.

```css
overflow: scroll;
```

### auto

Scrollbars appear only when needed.

```css
overflow: auto;
```

This is the value used most often.

## CSS Float

Before Flexbox and Grid became popular, **float** was commonly used to arrange elements side by side.

Even today, it's useful to know because older websites still use it.

### Float Left

```css
img {
    float: left;
}
```

The image moves to the left, and text wraps around it.

### Float Right

```css
img {
    float: right;
}
```

The image moves to the right.

### Clearing Float

Sometimes floating elements affect other elements below them.

To fix this, we use:

```css
clear: both;
```

## CSS Inline-block

Earlier, I learned that:

* Inline elements cannot have width and height.
* Block elements always take the full width.

`inline-block` gives the advantages of both.

### Example

```css
.card {
    display: inline-block;
    width: 200px;
    height: 150px;
}
```

Now multiple cards can appear on the same line while still having their own width and height.

This is useful for:

* Cards
* Buttons
* Small boxes
* Menu items

## Quick Recap

| Property                         | Purpose                                               |
| -------------------------------- | ----------------------------------------------------- |
| `display`                        | Controls how an element appears                       |
| `max-width`                      | Prevents elements from becoming too wide              |
| `position`                       | Places elements on the page                           |
| `top`, `bottom`, `left`, `right` | Moves positioned elements                             |
| `z-index`                        | Controls which element appears on top                 |
| `overflow`                       | Handles extra content inside an element               |
| `float`                          | Places elements side by side                          |
| `inline-block`                   | Keeps elements inline while allowing width and height |

## What I Learned

This section helped me understand how CSS controls the layout of a webpage.

Earlier, I only knew how to change colors and fonts. Now I understand how elements are arranged, how to move them, how overlapping works, and how different display types affect the page.

I also learned that while properties like **float** are still useful to know, modern websites mostly use **Flexbox** and **CSS Grid** for layouts. Still, understanding these basics makes it much easier to learn advanced layout techniques later.

## CSS Align

When I first started designing webpages, one thing I struggled with was aligning elements. Sometimes I wanted text in the center, sometimes I wanted an image in the middle, or a box in the center of the page.

CSS provides different ways to align elements depending on what we are trying to align.

### Align Text

```css
h1 {
    text-align: center;
}
```

Other values are:

* left
* right
* justify

### Center a Block Element

```css
.container {
    width: 400px;
    margin: auto;
}
```

`margin: auto;` is one of the easiest ways to center a block element.

### Center Using Flexbox

```css
.container {
    display: flex;
    justify-content: center;
    align-items: center;
}
```

This is the most common way to center content in modern websites.

## CSS Navigation Bars

Almost every website has a navigation bar.

It helps users move between different pages like **Home**, **About**, **Services**, and **Contact**.

Navigation bars are usually created using an unordered list.

### HTML

```html
<ul>
    <li><a href="#">Home</a></li>
    <li><a href="#">About</a></li>
    <li><a href="#">Contact</a></li>
</ul>
```

### CSS

```css
ul {
    list-style: none;
}

li {
    display: inline-block;
    margin-right: 20px;
}

a {
    text-decoration: none;
}
```

This removes bullets, places the items in one row, and removes the underline from links.

## CSS Dropdowns

A dropdown menu displays more options when the user hovers over or clicks a menu item.

Example:

```
Services
   ↓
Frontend
Backend
DevOps
```

### Basic HTML

```html
<div class="dropdown">
    <button>Services</button>

    <div class="content">
        <a href="#">Frontend</a>
        <a href="#">Backend</a>
        <a href="#">DevOps</a>
    </div>
</div>
```

### Basic CSS

```css
.content {
    display: none;
}

.dropdown:hover .content {
    display: block;
}
```

Initially, the menu is hidden.

When the mouse moves over **Services**, the menu becomes visible.

## CSS Image Gallery

Image galleries are used to display multiple images in an organized way.

Examples include:

* Portfolio websites
* Shopping websites
* Photography websites

Simple example:

```html
<img src="image1.jpg">
<img src="image2.jpg">
<img src="image3.jpg">
```

CSS

```css
img {
    width: 200px;
    margin: 10px;
}
```

Nowadays, image galleries are usually created using **Flexbox** or **Grid**.

## CSS Image Sprites

Instead of loading many small images separately, we can combine them into one large image.

This combined image is called an **image sprite**.

CSS then displays only the required part of the image.

### Why use image sprites?

* Faster page loading
* Fewer HTTP requests
* Better website performance

Although image sprites are less common today, it's still useful to know what they are.

## CSS Forms

Forms are used to collect information from users.

Examples include:

* Login forms
* Registration forms
* Contact forms

We can use CSS to make forms look cleaner.

Example

```css
input {
    width: 300px;
    padding: 10px;
}

button {
    background-color: blue;
    color: white;
    padding: 10px;
}
```

This makes input fields and buttons look much better.

## CSS Website Layout

A website is usually divided into different sections.

A common layout looks like this:

```text
-------------------------
        Header
-------------------------
      Navigation
-------------------------
 Main Content | Sidebar
-------------------------
        Footer
-------------------------
```

Each section has its own purpose.

### Header

Usually contains:

* Website logo
* Website title

### Navigation

Contains links to different pages.

### Main Content

This is where most of the webpage content is displayed.

### Sidebar

Often contains:

* Recent posts
* Categories
* Advertisements
* Extra links

### Footer

Usually contains:

* Copyright information
* Contact details
* Social media links

Nowadays, layouts are mostly created using **Flexbox** and **CSS Grid** because they are easier and more responsive.

## Quick Recap

| Topic          | What it does                            |
| -------------- | --------------------------------------- |
| Align          | Positions text and elements properly    |
| Navigation Bar | Helps users move between pages          |
| Dropdown       | Shows extra options when needed         |
| Image Gallery  | Displays multiple images neatly         |
| Image Sprite   | Combines many small images into one     |
| Forms          | Styles input fields and buttons         |
| Website Layout | Organizes the overall webpage structure |

## What I Learned

After learning these topics, I understood how a complete webpage is put together.

Earlier, I only knew how to style individual elements like headings and paragraphs. Now I know how to organize an entire webpage using navigation bars, forms, image galleries, and proper layouts.

I also learned that while some older techniques like **image sprites** are not used as much today, they are still good to know. For modern websites, **Flexbox** and **CSS Grid** are the preferred way to build responsive layouts.

