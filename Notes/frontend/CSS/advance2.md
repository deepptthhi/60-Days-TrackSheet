

## CSS 2D Transforms

Transforms change an element's position, size, or shape without
affecting the document layout.

### translate()

``` css
transform: translate(50px, 20px);
```

Moves an element.

### rotate()

``` css
transform: rotate(45deg);
```

Rotates the element.

### scale()

``` css
transform: scale(1.5);
```

Makes the element bigger or smaller.

### skew()

``` css
transform: skew(20deg, 10deg);
```

Tilts the element.

### Multiple Transforms

``` css
transform: translateX(20px) rotate(30deg) scale(1.2);
```


# CSS 3D Transforms

### rotateX()

``` css
transform: rotateX(60deg);
```

### rotateY()

``` css
transform: rotateY(60deg);
```

### rotateZ()

``` css
transform: rotateZ(45deg);
```

### perspective

``` css
perspective: 800px;
```

Adds depth for 3D effects.



# CSS Transitions

Transitions create smooth changes between property values.

``` css
.box{
    transition: all 0.3s ease;
}

.box:hover{
    background: royalblue;
}
```

Useful properties:

-   transition-property
-   transition-duration
-   transition-timing-function
-   transition-delay



# CSS Animations

Animations create movement without JavaScript.

``` css
@keyframes slide {
    from { transform: translateX(0); }
    to { transform: translateX(200px); }
}

.box{
    animation: slide 2s infinite;
}
```

Animation Properties

-   animation-name
-   animation-duration
-   animation-delay
-   animation-iteration-count
-   animation-direction
-   animation-fill-mode


# CSS Tooltips

Tooltip appears when the user hovers over an element.

``` html
<div class="tooltip">
    Hover Me
    <span class="tooltip-text">Hello!</span>
</div>
```

``` css
.tooltip{
    position: relative;
}

.tooltip-text{
    visibility: hidden;
}

.tooltip:hover .tooltip-text{
    visibility: visible;
}
```


# CSS Variables

Variables store reusable values.

``` css
:root{
    --primary: royalblue;
    --radius: 8px;
}

button{
    background: var(--primary);
    border-radius: var(--radius);
}
```

Benefits

-   Easy to maintain
-   Reusable
-   Consistent design


# CSS @property

Allows custom CSS properties to be animated.

``` css
@property --angle{
    syntax: "<angle>";
    inherits: false;
    initial-value: 0deg;
}
```

Mostly used for advanced animations.


# CSS Flexbox

Flexbox is a one-dimensional layout system.

## Flex Container

``` css
.container{
    display: flex;
}
```

Common Properties

``` css
justify-content: center;
align-items: center;
flex-direction: row;
flex-wrap: wrap;
gap: 20px;
```

justify-content values

-   flex-start
-   center
-   flex-end
-   space-between
-   space-around
-   space-evenly

align-items values

-   stretch
-   center
-   flex-start
-   flex-end

## Flex Items

``` css
.item{
    flex: 1;
    order: 2;
    align-self: center;
}
```

Useful Properties

-   flex-grow
-   flex-shrink
-   flex-basis
-   order
-   align-self

### Responsive Flexbox

``` css
.container{
    display:flex;
    flex-wrap:wrap;
    gap:20px;
}
```


# CSS Grid

Grid is a two-dimensional layout system.

## Grid Container

``` css
.container{
    display:grid;
    grid-template-columns:repeat(3,1fr);
    gap:20px;
}
```

Useful Properties

-   grid-template-columns
-   grid-template-rows
-   gap
-   justify-items
-   align-items

## Grid Items

``` css
.item{
    grid-column:1 / 3;
    grid-row:1 / 2;
}
```

## 12-Column Layout

``` css
.container{
    display:grid;
    grid-template-columns:repeat(12,1fr);
}

.main{
    grid-column:span 8;
}

.sidebar{
    grid-column:span 4;
}
```



# CSS @supports

Checks whether the browser supports a CSS feature.

``` css
@supports(display:grid){

.container{
    display:grid;
}

}
```

Useful for browser compatibility.



### Flexbox vs Grid

**Flexbox** - One-dimensional - Best for rows and columns

**Grid** - Two-dimensional - Best for complete page layouts

### Transform vs Transition

-   Transform changes the element.
-   Transition controls how smoothly the change happens.

### Transition vs Animation

-   Transition needs a trigger like `:hover`.
-   Animation can run automatically.


# Best Practices

-   Use Flexbox for small layouts.
-   Use Grid for full-page layouts.
-   Keep transition duration between 0.2s and 0.5s.
-   Avoid excessive animations.
-   Store colors and spacing using CSS variables.
-   Use `@supports` for newer CSS features.
