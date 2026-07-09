

## What is CSS?

When I first learned HTML, I noticed that the webpage only had the structure. It worked, but it looked very plain. That's where CSS comes in.

**CSS (Cascading Style Sheets)** is used to make a webpage look good. It helps us add colors, fonts, spacing, borders, layouts, animations, and much more.

In simple words:

* **HTML** builds the structure.
* **CSS** makes it attractive.

Without CSS, almost every website would look like plain text.

## Why Do We Use CSS?

CSS makes websites look clean and professional.

Some advantages are:

* It adds colors and styles.
* It changes fonts and text size.
* It controls spacing between elements.
* It helps create beautiful layouts.
* One CSS file can style many HTML pages.
* It makes websites easier to maintain.

## CSS Syntax

Every CSS rule has two parts:

* **Selector** → tells which HTML element to style.
* **Declaration** → tells what style to apply.

### Syntax

```css
selector {
    property: value;
}
```

### Example

```css
h1 {
    color: blue;
}
```

Here,

* `h1` is the selector.
* `color` is the property.
* `blue` is the value.

This changes the color of every `<h1>` heading to blue.

## CSS Selectors

Selectors tell CSS which HTML element should be styled.

### 1. Element Selector

It selects all elements with the same tag.

```css
p {
    color: green;
}
```

Every `<p>` tag becomes green.

### 2. ID Selector

An ID is unique.

Use `#` before the ID name.

HTML

```html
<h1 id="title">Welcome</h1>
```

CSS

```css
#title {
    color: red;
}
```

Only this heading becomes red.

### 3. Class Selector

A class can be used for multiple elements.

Use `.` before the class name.

HTML

```html
<p class="text">Hello</p>
<p class="text">Welcome</p>
```

CSS

```css
.text {
    color: blue;
}
```

Both paragraphs become blue.

### 4. Universal Selector

The universal selector selects every element.

```css
* {
    margin: 0;
    padding: 0;
}
```

It is commonly used to remove default spacing.

### 5. Group Selector

Sometimes we want to style multiple elements the same way.

```css
h1, h2, p {
    color: navy;
}
```

This applies the same style to all three elements.

## CSS Ways to Add Styles

There are three ways to use CSS.

### 1. Inline CSS

CSS is written inside the HTML tag.

```html
<h1 style="color:red;">Hello</h1>
```

This is useful for small changes but not recommended for large projects.

### 2. Internal CSS

CSS is written inside the `<style>` tag.

```html
<head>
    <style>
        h1 {
            color: blue;
        }
    </style>
</head>
```

Good for small websites or practice.

### 3. External CSS

CSS is written in a separate `.css` file.

HTML

```html
<link rel="stylesheet" href="style.css">
```

style.css

```css
h1 {
    color: blue;
}
```

This is the most commonly used method because it keeps HTML and CSS separate.

## CSS Comments

Comments are notes written for ourselves or other developers.

The browser ignores comments.

### Syntax

```css
/* This is a comment */
```

### Example

```css
/* Change heading color */

h1 {
    color: blue;
}
```

Comments make the code easier to understand.

## Common CSS Errors

When I started learning CSS, these were the mistakes I made most often.

### Missing Semicolon

Wrong

```css
h1 {
    color: blue
}
```

Correct

```css
h1 {
    color: blue;
}
```

### Wrong Property Name

Wrong

```css
h1 {
    colours: red;
}
```

Correct

```css
h1 {
    color: red;
}
```

### Wrong Selector

If the selector doesn't match the HTML element, the style won't be applied.

Always check the spelling of IDs and class names.

## CSS Colors

CSS provides different ways to add colors.

### Color Name

```css
h1 {
    color: red;
}
```

### HEX Value

```css
h1 {
    color: #ff0000;
}
```

### RGB

```css
h1 {
    color: rgb(255,0,0);
}
```

### RGBA

The last value controls transparency.

```css
h1 {
    color: rgba(255,0,0,0.5);
}
```

### HSL

```css
h1 {
    color: hsl(0,100%,50%);
}
```

As a beginner, using color names and HEX values is usually enough.

## CSS Backgrounds

Background properties change the background of an element.

### Background Color

```css
body {
    background-color: lightblue;
}
```

### Background Image

```css
body {
    background-image: url("image.jpg");
}
```

### Background Repeat

```css
body {
    background-repeat: no-repeat;
}
```

### Background Position

```css
body {
    background-position: center;
}
```

### Background Size

```css
body {
    background-size: cover;
}
```

This makes the image cover the entire element.

## CSS Borders

Borders are used to create an outline around an element.

### Border Width

```css
border-width: 2px;
```

### Border Style

```css
border-style: solid;
```

Some common border styles are:

* solid
* dotted
* dashed
* double

### Border Color

```css
border-color: blue;
```

### Shorthand

Instead of writing three lines, we can write:

```css
border: 2px solid black;
```

### Rounded Borders

```css
border-radius: 10px;
```

This gives rounded corners.

## What I Learned

After learning these topics, I understood that CSS is simply a collection of rules.

First, we choose **what** we want to style using a selector.

Then we decide **how** it should look using properties like `color`, `background`, and `border`.

The more I practiced changing colors, backgrounds, and borders, the easier CSS became to understand.

## CSS Margins

When I started designing webpages, I noticed that some elements were too close to each other. That's where **margin** helps.

Margin is the space **outside** an element's border. It creates space between two elements.

### Why do we use margin?

* To add space between elements.
* To make the webpage look clean.
* To improve readability.

### Syntax

```css
selector {
    margin: value;
}
```

### Example

```css
div {
    margin: 20px;
}
```

This adds **20px** of space on all four sides.

### Margin for Individual Sides

```css
div {
    margin-top: 20px;
    margin-right: 15px;
    margin-bottom: 20px;
    margin-left: 15px;
}
```

### Shorthand

All four sides

```css
margin: 20px;
```

Top-Bottom | Left-Right

```css
margin: 20px 10px;
```

Top | Left-Right | Bottom

```css
margin: 10px 20px 30px;
```

Top | Right | Bottom | Left

```css
margin: 10px 15px 20px 25px;
```

### Auto Margin

```css
div {
    width: 300px;
    margin: auto;
}
```

`margin: auto;` is commonly used to center an element horizontally.

## CSS Padding

At first, I thought margin and padding were the same. Later I understood that **padding is the space inside the border**, between the content and the border.

### Why do we use padding?

* To give content some breathing space.
* To make buttons and boxes look better.
* To improve readability.

### Syntax

```css
selector {
    padding: value;
}
```

### Example

```css
div {
    padding: 20px;
}
```

This adds 20px of space inside the element.

### Individual Padding

```css
padding-top: 20px;
padding-right: 10px;
padding-bottom: 20px;
padding-left: 10px;
```

### Shorthand

```css
padding: 20px;
```

```css
padding: 20px 10px;
```

```css
padding: 10px 15px 20px;
```

```css
padding: 10px 15px 20px 25px;
```

### Easy Way to Remember

**Margin → Outside the border**

**Padding → Inside the border**

## CSS Height and Width

Height and width decide the size of an element.

### Width

```css
div {
    width: 300px;
}
```

### Height

```css
div {
    height: 200px;
}
```

### Both Together

```css
div {
    width: 300px;
    height: 200px;
}
```

We can also use percentages.

```css
width: 50%;
```

Or viewport units.

```css
width: 100vw;
height: 100vh;
```

## CSS Box Model

The Box Model is one of the most important concepts in CSS.

Every HTML element is treated like a box.

A box has four parts.

```text
+-------------------------+
|        Margin           |
|  +-------------------+  |
|  |      Border       |  |
|  | +---------------+ |  |
|  | |   Padding     | |  |
|  | | +-----------+ | |  |
|  | | | Content   | | |  |
|  | | +-----------+ | |  |
|  | +---------------+ |  |
|  +-------------------+  |
+-------------------------+
```

### Content

The actual text, image, or anything inside the element.

### Padding

Space between the content and border.

### Border

The outline around the element.

### Margin

Space outside the border.

### Why is the Box Model important?

Understanding the Box Model helps us:

* Create better layouts.
* Add proper spacing.
* Fix alignment issues.
* Design responsive webpages.

## CSS Outline

An outline is another line drawn around an element.

Unlike a border, it does **not** take up extra space.

### Syntax

```css
outline: 2px solid red;
```

### Example

```css
button {
    outline: 2px solid blue;
}
```

### Difference Between Border and Outline

| Border                | Outline               |
| --------------------- | --------------------- |
| Takes space           | Doesn't take space    |
| Part of the box model | Outside the box model |

## CSS Text

CSS allows us to style text in different ways.

### Text Color

```css
p {
    color: blue;
}
```

### Text Alignment

```css
text-align: center;
```

Other values are:

* left
* right
* justify

### Text Decoration

```css
text-decoration: underline;
```

Remove underline from links

```css
text-decoration: none;
```

### Text Transform

Uppercase

```css
text-transform: uppercase;
```

Lowercase

```css
text-transform: lowercase;
```

Capitalize

```css
text-transform: capitalize;
```

### Letter Spacing

```css
letter-spacing: 2px;
```

### Word Spacing

```css
word-spacing: 10px;
```

### Line Height

```css
line-height: 2;
```

This increases the space between lines.

## CSS Fonts

Fonts decide how text looks.

### Font Family

```css
font-family: Arial;
```

Multiple fonts can be given.

```css
font-family: Arial, Helvetica, sans-serif;
```

If one font isn't available, the browser uses the next one.

### Font Size

```css
font-size: 20px;
```

### Font Weight

```css
font-weight: bold;
```

Other values:

* normal
* lighter
* bolder
* 100–900

### Font Style

```css
font-style: italic;
```

### Shorthand

```css
font: italic bold 20px Arial;
```

## CSS Icons

Instead of using images for icons, websites often use icon libraries.

Popular libraries are:

* Font Awesome
* Bootstrap Icons
* Google Material Icons

Example

```html
<i class="fa-solid fa-house"></i>
```

Icons make websites look modern and are easy to customize using CSS.

## CSS Links

Links are created using the `<a>` tag.

CSS helps change their appearance.

### Example

```css
a {
    color: blue;
}
```

Remove underline

```css
a {
    text-decoration: none;
}
```

### Link States

```css
a:link
```

Normal link

```css
a:visited
```

Visited link

```css
a:hover
```

Mouse is over the link

```css
a:active
```

Link is being clicked

Example

```css
a:hover {
    color: red;
}
```

## CSS Lists

CSS can style ordered and unordered lists.

### Bullet Style

```css
list-style-type: square;
```

Other values:

* disc
* circle
* none

### Number Style

```css
list-style-type: upper-roman;
```

### Remove Bullets

```css
list-style: none;
```

This is commonly used while creating navigation bars.

## CSS Tables

CSS makes tables look neat and easy to read.

### Border

```css
table, th, td {
    border: 1px solid black;
}
```

### Border Collapse

```css
border-collapse: collapse;
```

This removes the double border.

### Padding

```css
th, td {
    padding: 10px;
}
```

### Text Alignment

```css
text-align: center;
```

### Alternate Row Colors

```css
tr:nth-child(even) {
    background-color: lightgray;
}
```

This improves readability for large tables.

## Quick Recap

* **Margin** → Space outside an element.
* **Padding** → Space inside an element.
* **Height & Width** → Control element size.
* **Box Model** → Every element has Content, Padding, Border, and Margin.
* **Outline** → Similar to a border but doesn't take space.
* **Text** → Styles text using color, alignment, spacing, and decoration.
* **Fonts** → Change the font family, size, style, and weight.
* **Icons** → Add symbols using icon libraries.
* **Links** → Style hyperlinks and their different states.
* **Lists** → Customize bullets and numbering.
* **Tables** → Improve the appearance of tables with borders, spacing, and alignment.

## What I Learned

This part of CSS helped me understand how websites become neat and organized. Earlier, I only knew how to change colors, but now I know how to control spacing, size, fonts, tables, and text.

The biggest concept I learned here is the **CSS Box Model**. Once I understood the difference between **margin**, **border**, **padding**, and **content**, designing layouts became much easier. I also realized that good spacing and readable text make a huge difference in how a webpage looks.

