


## What is React?

React is a JavaScript library used to build fast and interactive user
interfaces (UI). Instead of updating an entire webpage, React updates
only the parts that change.

### Why use React?

-   Reusable components
-   Faster rendering with Virtual DOM
-   Easy to maintain
-   Large community support



## Simple Explanation

React lets us divide a website into small reusable pieces called
**components**.

Example: - Navbar - Sidebar - Footer - Login Form

Each can be created once and reused.



# React Get Started

## Installation

``` bash
npx create-react-app my-app
cd my-app
npm start
```

OR (recommended)

``` bash
npm create vite@latest
cd project-name
npm install
npm run dev
```



# React First App

``` jsx
function App() {
  return <h1>Hello React!</h1>;
}

export default App;
```

Explanation: - App is a component. - It returns HTML using JSX. - export
default makes it available elsewhere.



# React Render HTML

``` jsx
const root = ReactDOM.createRoot(document.getElementById("root"));
root.render(<App />);
```

React renders the App component inside the HTML element with id="root".


# React Upgrade

Upgrade React with:

``` bash
npm update react react-dom
```

Always back up your project before major upgrades.



# React ES6

React commonly uses ES6 features:

## Arrow Function

``` javascript
const greet = () => {
  return "Hello";
};
```

## Destructuring

``` javascript
const person = {
  name: "Deepthi",
  age: 22
};

const { name, age } = person;
```

## Spread Operator

``` javascript
const a = [1,2];
const b = [...a,3];
```



# JSX Intro

JSX lets us write HTML inside JavaScript.

``` jsx
const element = <h1>Hello World</h1>;
```

React converts JSX into JavaScript.

Rules: - One parent element - Close every tag - Use className instead of
class



# JSX Expressions

Expressions go inside curly braces.

``` jsx
const name = "Deepthi";

function App(){
  return <h1>Hello {name}</h1>;
}
```



# JSX Attributes

``` jsx
<img src="logo.png" alt="Logo" />
```

``` jsx
<div className="container">
```

Use camelCase for event names and many attributes.


# JSX If Statements

Use conditions to render UI.

## if statement

``` jsx
function App(){
  const isLoggedIn = true;

  if(isLoggedIn){
    return <h1>Welcome</h1>;
  }

  return <h1>Please Login</h1>;
}
```

## Ternary Operator

``` jsx
<h1>{isLoggedIn ? "Welcome" : "Login First"}</h1>
```

## Logical AND

``` jsx
{isAdmin && <button>Delete</button>}
```


# Quick Revision

-   React is a JavaScript library.
-   Everything is built using components.
-   JSX looks like HTML but runs inside JavaScript.
-   Expressions use {}.
-   Use className instead of class.
-   ReactDOM renders components.
-   ES6 features are heavily used.


