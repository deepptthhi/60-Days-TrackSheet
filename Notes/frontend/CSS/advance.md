
## CSS Combinators

While learning CSS, I came across situations where I didn't want to style every element. I only wanted to style elements based on their relationship with other elements. That's where **combinators** are useful.

### Why do we use combinators?

* To target specific elements.
* To avoid writing unnecessary classes.
* To make CSS more organized.

There are four main combinators.

### Descendant Selector (Space)

It selects all matching elements inside another element.

### Syntax

```css
div p {
    color: blue;
}
```

### Example

```html
<div>
    <p>Hello</p>
    <section>
        <p>Welcome</p>
    </section>
</div>
```

Both paragraphs become blue because they are inside the `div`.

### Child Selector (>)

It selects only the direct children.

### Syntax

```css
div > p {
    color: red;
}
```

Only the `<p>` that is directly inside the `div` is selected.

### Adjacent Sibling Selector (+)

It selects the immediate next sibling.

```css
h1 + p {
    color: green;
}
```

Only the first paragraph immediately after the `<h1>` is selected.

### General Sibling Selector (~)

It selects all matching siblings after an element.

```css
h1 ~ p {
    color: orange;
}
```

Every paragraph that comes after the `<h1>` becomes orange.

### Easy Way to Remember

* Space → Any child inside.
* `>` → Direct child only.
* `+` → Next sibling only.
* `~` → All following siblings.

## CSS Pseudo-classes

Pseudo-classes let us style an element based on its state.

For example:

* Mouse is over a button.
* A link has already been visited.
* A text box is selected.

### Syntax

```css
selector:pseudo-class {
    property: value;
}
```

### :hover

Changes the style when the mouse is over an element.

```css
button:hover {
    background-color: blue;
    color: white;
}
```

### :active

Applied while an element is being clicked.

```css
button:active {
    background-color: red;
}
```

### :visited

Changes the appearance of visited links.

```css
a:visited {
    color: purple;
}
```

### :focus

Used when an input box is selected.

```css
input:focus {
    border: 2px solid blue;
}
```

### :first-child

Selects the first child.

```css
li:first-child {
    color: red;
}
```

### :last-child

Selects the last child.

```css
li:last-child {
    color: blue;
}
```

### :nth-child()

Selects a specific child.

```css
li:nth-child(3) {
    color: green;
}
```

This selects the third list item.

## CSS Pseudo-elements

Pseudo-elements allow us to style a specific part of an element.

### Syntax

```css
selector::pseudo-element
```

### ::before

Adds content before an element.

```css
h1::before {
    content: "★ ";
}
```

### ::after

Adds content after an element.

```css
h1::after {
    content: " ✔";
}
```

### ::first-letter

Styles only the first letter.

```css
p::first-letter {
    font-size: 30px;
}
```

### ::first-line

Styles only the first line.

```css
p::first-line {
    color: blue;
}
```

### ::selection

Changes the color of selected text.

```css
::selection {
    background-color: yellow;
}
```

## CSS Attribute Selectors

Sometimes we want to style elements based on their attributes.

Instead of using classes or IDs, we can use attribute selectors.

### Select by Attribute

```css
input[type] {
    border: 1px solid black;
}
```

### Select a Specific Attribute Value

```css
input[type="text"] {
    background-color: lightgray;
}
```

### Links Starting with HTTPS

```css
a[href^="https"] {
    color: green;
}
```

### Links Ending with .pdf

```css
a[href$=".pdf"] {
    color: red;
}
```

Attribute selectors make CSS more flexible and reduce the need for extra classes.

## CSS Opacity

Opacity controls how transparent an element is.

The value ranges from **0 to 1**.

* 0 → Completely invisible
* 1 → Fully visible

### Syntax

```css
opacity: 0.5;
```

### Example

```css
img {
    opacity: 0.7;
}
```

This makes the image slightly transparent.

A common hover effect is:

```css
img:hover {
    opacity: 1;
}
```

## CSS Counters

CSS can automatically number elements.

This is useful for headings, chapters, or lists.

### Example

```css
body {
    counter-reset: section;
}

h2::before {
    counter-increment: section;
    content: "Section " counter(section) ": ";
}
```

Output:

```text
Section 1: Introduction
Section 2: HTML
Section 3: CSS
```

## CSS Units

Units tell CSS how big or small something should be.

### px (Pixels)

Fixed size.

```css
font-size: 20px;
```

### %

Relative to the parent element.

```css
width: 50%;
```

### em

Relative to the parent font size.

```css
font-size: 2em;
```

### rem

Relative to the root (`html`) font size.

```css
font-size: 2rem;
```

Many developers prefer `rem` because it gives more consistent results.

### vw (Viewport Width)

Based on the browser width.

```css
width: 50vw;
```

### vh (Viewport Height)

Based on the browser height.

```css
height: 100vh;
```

### Easy Way to Remember

| Unit | Meaning                 |
| ---- | ----------------------- |
| px   | Fixed size              |
| %    | Relative to parent      |
| em   | Relative to parent font |
| rem  | Relative to root font   |
| vw   | Viewport width          |
| vh   | Viewport height         |

## What I Learned

This section showed me that CSS can do much more than just change colors and fonts.

I learned how to target elements more precisely using combinators and attribute selectors. Pseudo-classes helped me create interactive effects like hover and focus, while pseudo-elements allowed me to style specific parts of an element.

I also understood the difference between CSS units like `px`, `%`, `em`, and `rem`, which will help me build websites that work better on different screen sizes.

## CSS Inheritance

While learning CSS, I noticed that sometimes I didn't have to write the same style for every element. That's because some CSS properties are automatically passed from a parent element to its child elements. This is called **inheritance**.

For example, if I change the text color of a `<div>`, the text inside it usually gets the same color.

### Example

HTML

```html
<div>
    <h1>Welcome</h1>
    <p>This is CSS.</p>
</div>
```

CSS

```css
div {
    color: blue;
}
```

Both the heading and paragraph become blue because the `color` property is inherited.

### Properties that are commonly inherited

* `color`
* `font-family`
* `font-size`
* `text-align`
* `visibility`

### Properties that are **not** inherited

* `margin`
* `padding`
* `border`
* `width`
* `height`
* `background`

### Force Inheritance

Sometimes we can use the `inherit` value.

```css
p {
    color: inherit;
}
```

This tells the paragraph to use the same color as its parent.

## CSS Specificity

Sometimes I wrote multiple CSS rules for the same element and wondered why only one of them worked.

That's because CSS follows something called **specificity**.

Specificity decides which CSS rule has the highest priority.

### Example

```css
p {
    color: blue;
}
```

```css
.text {
    color: green;
}
```

```css
#title {
    color: red;
}
```

If a paragraph has both a class and an ID, the **ID selector wins** because it has higher priority.

### Priority Order

Highest ⬇️

1. Inline CSS
2. ID Selector (`#`)
3. Class Selector (`.`)
4. Element Selector (`p`, `h1`)
5. Universal Selector (`*`)

### Example

HTML

```html
<p id="title" class="text">Hello</p>
```

CSS

```css
p {
    color: blue;
}

.text {
    color: green;
}

#title {
    color: red;
}
```

Output:

The text becomes **red** because the ID selector has the highest priority.

### Easy Way to Remember

**Inline > ID > Class > Element > Universal**

## CSS !important

Normally, CSS follows the specificity rules.

But if we add `!important`, that rule gets the highest priority.

### Syntax

```css
color: red !important;
```

### Example

```css
p {
    color: blue;
}

p {
    color: red !important;
}
```

Output:

The paragraph becomes **red**.

### Should we always use `!important`?

No.

It should only be used when absolutely necessary because it makes CSS harder to manage.

Most of the time, it's better to fix the selector instead of using `!important`.

## CSS Math Functions

CSS provides some built-in math functions that make layouts more flexible.

### calc()

`calc()` performs calculations.

Example

```css
width: calc(100% - 50px);
```

This means:

Take the full width and subtract 50 pixels.

### min()

Returns the smaller value.

```css
width: min(500px, 90%);
```

The browser chooses whichever value is smaller.

### max()

Returns the larger value.

```css
width: max(400px, 60%);
```

The browser chooses the larger value.

### clamp()

`clamp()` keeps a value between a minimum and maximum.

```css
font-size: clamp(16px, 3vw, 30px);
```

This is very useful for responsive websites because the font size changes with the screen size but never becomes too small or too large.

## CSS Optimization

As I learned more CSS, I realized it's not just about making websites look good. It's also important to keep the code clean and easy to maintain.

Some good practices are:

* Use meaningful class names.
* Avoid writing the same CSS again and again.
* Remove unused CSS.
* Keep related styles together.
* Use external CSS files instead of inline CSS.
* Write simple and readable code.
* Use comments when needed.

Writing clean CSS makes projects easier to understand and update later.

## CSS Accessibility

Accessibility means making websites easy for **everyone** to use, including people with disabilities.

A good website should be usable even if someone has difficulty seeing, hearing, or using a mouse.

### Some simple accessibility practices

Use good color contrast.

✅ Easy to read

```css
color: black;
background: white;
```

Avoid very light text on a light background.

Use readable font sizes.

```css
font-size: 16px;
```

Don't remove keyboard focus unless necessary.

Make buttons and links easy to click.

Write meaningful link text.

Instead of:

```text
Click Here
```

Write:

```text
Download CSS Notes
```

Accessibility helps create better websites for everyone.

## Quick Recap

| Topic          | What I understood                                                       |
| -------------- | ----------------------------------------------------------------------- |
| Inheritance    | Some CSS properties are passed from parent to child.                    |
| Specificity    | CSS decides which rule should be applied based on priority.             |
| !important     | Gives a rule the highest priority, but should be used carefully.        |
| Math Functions | `calc()`, `min()`, `max()`, and `clamp()` help create flexible layouts. |
| Optimization   | Clean and organized CSS is easier to maintain.                          |
| Accessibility  | Websites should be easy for everyone to use.                            |

## What I Learned

After finishing CSS, I realized it's much more than changing colors and fonts. CSS controls almost every part of how a webpage looks and feels.

The biggest things I learned were the **Box Model**, **Display**, **Position**, **Flexbox basics through alignment**, **Selectors**, and **Specificity**. Understanding these concepts made it much easier to see how real websites are built.

I also understood that writing CSS isn't just about making a page attractive. Good CSS should be clean, responsive, and accessible so that it works well on different devices and is easy for everyone to use.

The best way to improve at CSS is by building small projects and practicing regularly. The more I experiment with different properties and layouts, the more comfortable I become with designing webpages.
