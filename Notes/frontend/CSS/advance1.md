
## CSS Image Styling

CSS provides many properties to make images look better and fit well on
a webpage.

### Rounded Images

``` css
img {
    border-radius: 10px;
}
```

Makes the image corners rounded.

### Circular Images

``` css
img {
    border-radius: 50%;
}
```

Used for profile pictures and avatars.

### Responsive Images

``` css
img {
    max-width: 100%;
    height: auto;
}
```

-   `max-width: 100%` prevents the image from overflowing its container.
-   `height: auto` keeps the image's aspect ratio.

### Thumbnail Images

``` css
img {
    border: 1px solid gray;
    padding: 5px;
    border-radius: 5px;
}
```

Commonly used in galleries.


# CSS Image Modal

An image modal displays a larger version of an image when the user
clicks on it.

### How it works

1.  User clicks an image.
2.  A popup (modal) opens.
3.  The larger image is displayed.
4.  User closes the popup.

Usually created using HTML, CSS, and JavaScript.


# CSS Image Centering

## Using Margin

``` css
img {
    display: block;
    margin: auto;
}
```

## Using Flexbox

``` css
.container {
    display: flex;
    justify-content: center;
    align-items: center;
}
```


# CSS Image Filters

``` css
filter: blur(5px);
filter: brightness(150%);
filter: contrast(200%);
filter: grayscale(100%);
filter: sepia(100%);
filter: invert(100%);
filter: opacity(50%);
filter: drop-shadow(5px 5px 8px gray);
filter: grayscale(100%) blur(2px);
```


# CSS Image Shapes

``` css
border-radius: 50%;
border-radius: 50% / 30%;
clip-path: circle();
clip-path: polygon(50% 0%,100% 100%,0% 100%);
```


# CSS object-fit

``` css
img {
    width: 300px;
    height: 200px;
    object-fit: cover;
}
```

Values: - fill - contain - cover - none - scale-down


# CSS object-position

``` css
object-position: center;
object-position: top;
object-position: bottom;
object-position: left;
object-position: right;
```


# CSS Masking

``` css
mask-image: url(mask.png);
```

Other properties: - mask-size - mask-position - mask-repeat


# CSS Buttons

``` css
button {
    background: royalblue;
    color: white;
    padding: 12px 20px;
    border: none;
    border-radius: 8px;
    cursor: pointer;
}

button:hover {
    background: blue;
}

button:disabled {
    opacity: 0.5;
    cursor: not-allowed;
}
```



# CSS Pagination

``` html
<div class="pagination">
    <a href="#">1</a>
    <a href="#">2</a>
    <a href="#">3</a>
</div>
```

``` css
.pagination a {
    padding: 10px;
    text-decoration: none;
}

.active {
    background: royalblue;
    color: white;
}
```


# CSS Multiple Columns

``` css
column-count: 3;
column-gap: 30px;
column-rule: 2px solid gray;
column-width: 250px;
```



# CSS User Interface

``` css
resize: both;
overflow: auto;

cursor: pointer;

outline: 2px solid blue;
```


# CSS Box Sizing

``` css
* {
    box-sizing: border-box;
}
```

This includes padding and borders inside the specified width and height.

# Best Practices

-   Make images responsive using `max-width: 100%`.
-   Use `object-fit: cover` for cards and hero sections.
-   Avoid using too many filters together.
-   Keep button styles consistent.
-   Use `cursor: pointer` for clickable elements.
-   Apply `box-sizing: border-box` globally.
