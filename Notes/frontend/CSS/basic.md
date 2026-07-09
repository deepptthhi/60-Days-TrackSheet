

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
