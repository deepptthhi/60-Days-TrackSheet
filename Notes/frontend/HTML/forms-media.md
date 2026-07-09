

## What are HTML Forms?

Forms are used to collect information from users. Whenever we sign in,
register, search, or submit feedback, we are using an HTML form.

The `<form>` tag acts as a container for different input fields.

### Syntax

``` html
<form>
</form>
```

## Form Attributes

Some common form attributes are:

-   `action` -- Where the form data is sent.
-   `method` -- How the data is sent (`GET` or `POST`).
-   `autocomplete` -- Enables or disables suggestions.
-   `target` -- Opens the response in a new tab or the same tab.

### Example

``` html
<form action="/submit" method="post">
</form>
```

## Form Elements

Forms can contain different elements.

-   `<input>`
-   `<label>`
-   `<textarea>`
-   `<select>`
-   `<option>`
-   `<button>`
-   `<fieldset>`
-   `<legend>`

These elements help us collect different types of user input.

## Labels

A label tells the user what an input field is for.

Example

``` html
<label for="name">Name</label>
<input type="text" id="name">
```

Using labels also improves accessibility.

## Input Types

The `type` attribute changes the behavior of an input field.

Common input types are:

-   text
-   password
-   email
-   number
-   date
-   time
-   color
-   file
-   checkbox
-   radio
-   submit
-   reset
-   search

### Example

``` html
<input type="email">
<input type="password">
<input type="date">
```

## Input Attributes

Input attributes give more control over user input.

Common attributes:

-   placeholder
-   value
-   required
-   readonly
-   disabled
-   maxlength
-   minlength
-   min
-   max
-   step
-   autofocus
-   checked

### Example

``` html
<input type="text" placeholder="Enter your name" required>
```

Here, `placeholder` shows a hint and `required` prevents the form from
being submitted if the field is empty.

## Select Dropdown

A dropdown allows users to choose one option.

``` html
<select>
<option>HTML</option>
<option>CSS</option>
<option>JavaScript</option>
</select>
```

## Textarea

A textarea is used when users need to enter multiple lines of text.

``` html
<textarea rows="4" cols="30"></textarea>
```

## Checkbox

Checkboxes allow users to select multiple options.

``` html
<input type="checkbox"> HTML
<input type="checkbox"> CSS
```

## Radio Button

Radio buttons allow users to select only one option.

``` html
<input type="radio" name="gender"> Male
<input type="radio" name="gender"> Female
```

The `name` attribute groups radio buttons together.

## Buttons

Buttons submit forms or perform actions.

``` html
<button>Submit</button>
```

Common button types:

-   submit
-   reset
-   button

## HTML Canvas

Canvas is used to draw graphics using JavaScript.

Example uses:

-   Games
-   Charts
-   Animations
-   Drawing applications

``` html
<canvas id="canvas"></canvas>
```

Canvas needs JavaScript to draw shapes.

## HTML SVG

SVG stands for **Scalable Vector Graphics**.

Unlike normal images, SVG graphics stay clear even when zoomed.

Common uses:

-   Logos
-   Icons
-   Charts
-   Illustrations

``` html
<svg width="100" height="100">
<circle cx="50" cy="50" r="40"/>
</svg>
```

## HTML Audio

The `<audio>` tag plays sound on a webpage.

``` html
<audio controls>
<source src="song.mp3">
</audio>
```

The `controls` attribute displays play and pause buttons.

## HTML Video

Videos are displayed using the `<video>` tag.

``` html
<video controls width="400">
<source src="movie.mp4">
</video>
```

Useful attributes:

-   controls
-   autoplay
-   muted
-   loop
-   poster

## HTML YouTube

Instead of uploading a video, we can embed a YouTube video using an
iframe.

``` html
<iframe
src="https://www.youtube.com/embed/VIDEO_ID">
</iframe>
```

This is commonly used in blogs and tutorials.

## HTML Plug-ins

Earlier, plug-ins were used to display multimedia content.

Examples:

-   Flash
-   Java Applets

Today, most plug-ins are no longer used because HTML5 supports audio,
video and graphics directly.

## Things I Learned

-   Forms collect user input.
-   Labels make forms easier to understand.
-   Different input types are used for different data.
-   Validation can be done using HTML attributes like `required`.
-   Canvas uses JavaScript for drawing.
-   SVG creates scalable graphics.
-   HTML5 supports audio and video without external plug-ins.

## Common Mistakes

-   Forgetting labels for input fields.
-   Using the wrong input type.
-   Not validating required fields.
-   Uploading huge media files without optimization.
-   Using plug-ins instead of HTML5 features.

## Quick Revision

-   Forms collect data.
-   Input types change field behavior.
-   Labels improve accessibility.
-   Canvas draws graphics.
-   SVG creates scalable images.
-   Audio and video are supported in HTML5.
-   YouTube videos can be embedded using an iframe.
