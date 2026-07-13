

# React Portals

## What are Portals?

Normally, React renders components inside the root element. Portals
allow us to render a component somewhere else in the DOM.

### Why use Portals?

-   Modals (Popups)
-   Dialog Boxes
-   Tooltips
-   Notifications

### Syntax

``` jsx
import { createPortal } from "react-dom";

function Modal() {
  return createPortal(
    <h2>This is a Modal</h2>,
    document.getElementById("portal-root")
  );
}
```



# React Suspense

## What is Suspense?

Suspense allows React to display a fallback UI while waiting for a
component to load.

### Example

``` jsx
import { Suspense, lazy } from "react";

const Home = lazy(() => import("./Home"));

function App() {
  return (
    <Suspense fallback={<h2>Loading...</h2>}>
      <Home />
    </Suspense>
  );
}
```


# React CSS Styling

CSS can be applied just like normal CSS.

``` jsx
import "./App.css";

function App() {
  return <h1 className="title">Hello</h1>;
}
```



# React CSS Modules

CSS Modules prevent class name conflicts.

### App.module.css

``` css
.title{
    color:blue;
}
```

### App.jsx

``` jsx
import styles from "./App.module.css";

<h1 className={styles.title}>Hello</h1>
```



# React CSS-in-JS

CSS can also be written directly inside JavaScript.

``` jsx
const headingStyle = {
  color: "blue",
  fontSize: "30px"
};

function App() {
  return <h1 style={headingStyle}>Hello</h1>;
}
```



# React Router

React Router is used to move between different pages without refreshing
the website.

### Installation

``` bash
npm install react-router-dom
```

### Example

``` jsx
import { BrowserRouter, Routes, Route } from "react-router-dom";

function App() {
  return (
    <BrowserRouter>
      <Routes>
        <Route path="/" element={<Home />} />
        <Route path="/about" element={<About />} />
      </Routes>
    </BrowserRouter>
  );
}
```



# React Transitions

Transitions make UI changes smoother.

Common uses: - Fade Animation - Slide Animation - Loading Animation

Libraries like **react-transition-group** are commonly used.



# React Forward Ref

Normally refs cannot be passed directly to child components.

forwardRef allows parent components to access child DOM elements.

### Example

``` jsx
import { forwardRef } from "react";

const Input = forwardRef((props, ref) => {
  return <input ref={ref} />;
});
```


# React Higher Order Components (HOC)

## What is HOC?

A Higher Order Component is a function that takes another component and
returns a new component with extra functionality.

Think of it as wrapping one component with another.

### Example

``` jsx
function withMessage(Component){
    return function(){
        return (
            <>
                <h2>Welcome</h2>
                <Component/>
            </>
        );
    };
}
```


# React Sass

Sass is an advanced version of CSS.

It supports: - Variables - Nesting - Mixins - Better organization

### Installation

``` bash
npm install sass
```

### Example

``` scss
$color: blue;

h1{
    color:$color;
}
```

Import it like:

``` jsx
import "./App.scss";
```


# Best Practices

-   Use Portals for Modals.
-   Use Suspense with lazy loading.
-   Prefer CSS Modules in large projects.
-   Use React Router for multi-page applications.
-   Use forwardRef only when necessary.
-   Use HOCs only when reusable logic is required.
-   Use Sass for better CSS organization.



# Quick Revision

-   Portals render outside the root.
-   Suspense shows loading UI.
-   CSS Modules avoid class conflicts.
-   CSS-in-JS stores styles inside JavaScript.
-   React Router handles navigation.
-   Transitions improve user experience.
-   forwardRef accesses child elements.
-   HOC adds reusable functionality.
-   Sass extends CSS.


