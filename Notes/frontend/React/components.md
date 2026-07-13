

# React Components

## What are Components?

Components are small, reusable pieces of UI. Instead of writing the same
HTML again and again, we create a component once and use it wherever
needed.

Examples: - Navbar - Footer - Login Form - Product Card

### Syntax

``` jsx
function Welcome() {
  return <h1>Welcome!</h1>;
}

export default Welcome;
```

### Using a Component

``` jsx
import Welcome from "./Welcome";

function App() {
  return (
    <div>
      <Welcome />
    </div>
  );
}
```



# React Class Components

Before Hooks, React applications were often built using class
components.

### Syntax

``` jsx
import React, { Component } from "react";

class Welcome extends Component {
  render() {
    return <h1>Hello React</h1>;
  }
}

export default Welcome;
```

### Note

Today, functional components are preferred because they are simpler and
support Hooks.



# React Props

## What are Props?

Props (Properties) are used to pass data from a parent component to a
child component.

Think of props like function parameters.

### Syntax

``` jsx
function Student(props) {
  return <h2>{props.name}</h2>;
}
```

### Example

``` jsx
function App() {
  return (
    <>
      <Student name="Deepthi" />
      <Student name="Rahul" />
    </>
  );
}
```

Output:

    Deepthi
    Rahul



# Props Destructuring

Instead of writing props.name every time, we can destructure.

### Without Destructuring

``` jsx
function Student(props) {
  return <h1>{props.name}</h1>;
}
```

### With Destructuring

``` jsx
function Student({ name, age }) {
  return (
    <>
      <h1>{name}</h1>
      <p>{age}</p>
    </>
  );
}
```

This makes the code cleaner.


# Props Children

The special prop **children** represents everything placed between
opening and closing tags.

### Example

``` jsx
function Card({ children }) {
  return (
    <div className="card">
      {children}
    </div>
  );
}
```

Usage

``` jsx
<Card>
  <h2>React Notes</h2>
  <p>Learning Components</p>
</Card>
```

Output

    React Notes
    Learning Components



# React Events

Events allow React to respond to user actions.

Examples: - Click - Double Click - Mouse Hover - Keyboard Input

### Syntax

``` jsx
function App() {
  function greet() {
    alert("Hello!");
  }

  return <button onClick={greet}>Click Me</button>;
}
```

### Passing Parameters

``` jsx
<button onClick={() => greet("Deepthi")}>
  Click
</button>
```



# React Conditionals

Sometimes we want to display different UI depending on a condition.

### if Statement

``` jsx
if (isLoggedIn) {
  return <Home />;
}

return <Login />;
```

### Ternary Operator

``` jsx
{isLoggedIn ? <Home /> : <Login />}
```

### Logical AND

``` jsx
{isAdmin && <button>Delete</button>}
```



# React Lists

Lists help display multiple items dynamically.

### Using map()

``` jsx
const fruits = ["Apple", "Banana", "Mango"];

function App() {
  return (
    <ul>
      {fruits.map((fruit) => (
        <li>{fruit}</li>
      ))}
    </ul>
  );
}
```

### Using Keys

Always provide a unique key.

``` jsx
const users = [
  { id: 1, name: "Deepthi" },
  { id: 2, name: "Rahul" }
];

function App() {
  return (
    <>
      {users.map(user => (
        <h2 key={user.id}>
          {user.name}
        </h2>
      ))}
    </>
  );
}
```

Why keys?

-   Improve performance
-   Help React identify changed items
-   Prevent rendering issues



# Best Practices

-   Keep components small and reusable.
-   Use functional components whenever possible.
-   Pass data using props.
-   Destructure props for cleaner code.
-   Always add a unique key while rendering lists.
-   Keep event handler functions simple.



# Quick Revision

-   Components are reusable UI blocks.
-   Functional components are preferred over class components.
-   Props pass data from parent to child.
-   Children represents nested content.
-   Events respond to user interactions.
-   Conditionals display UI based on conditions.
-   map() is used to render lists.
-   Always use unique keys.


