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
