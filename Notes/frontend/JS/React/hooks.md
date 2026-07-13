

# What are Hooks?

## Simple Explanation

Hooks are special functions introduced in **React 16.8** that allow
functional components to use features like state, lifecycle methods,
context, and more.

Before Hooks, these features were only available in class components.

### Why use Hooks?

-   Write less code
-   Reuse logic easily
-   Easier to understand
-   No need for class components

**Rule:** Hooks can only be called at the top level of a functional
component or inside a custom hook.


# useState

## What is useState?

`useState` is used to create and update state (data that can change).

### Syntax

``` jsx
import { useState } from "react";

const [count, setCount] = useState(0);
```

-   `count` → current value
-   `setCount()` → updates the value

### Example

``` jsx
import { useState } from "react";

function Counter() {
  const [count, setCount] = useState(0);

  return (
    <>
      <h2>{count}</h2>
      <button onClick={() => setCount(count + 1)}>
        Increment
      </button>
    </>
  );
}
```


# useEffect

## What is useEffect?

`useEffect` performs side effects such as: - Fetching API data -
Updating the page title - Timers - Event listeners

### Syntax

``` jsx
useEffect(() => {
  // code here
}, []);
```

### Example

``` jsx
import { useEffect } from "react";

function App() {
  useEffect(() => {
    console.log("Component Loaded");
  }, []);

  return <h1>Hello React</h1>;
}
```

### Dependency Array

``` jsx
useEffect(() => {}, []);
```

Runs once.

``` jsx
useEffect(() => {});
```

Runs after every render.

``` jsx
useEffect(() => {}, [count]);
```

Runs whenever `count` changes.



# useContext

## What is useContext?

It allows data to be shared across components without passing props
manually.

### Create Context

``` jsx
import { createContext } from "react";

const UserContext = createContext();
```

### Use Context

``` jsx
import { useContext } from "react";

const user = useContext(UserContext);
```

Useful for: - Theme - Logged-in user - Language - Settings



# useRef

## What is useRef?

`useRef` stores a value without causing a re-render.

It is commonly used to access DOM elements.

### Example

``` jsx
import { useRef } from "react";

function App() {
  const inputRef = useRef();

  function focusInput() {
    inputRef.current.focus();
  }

  return (
    <>
      <input ref={inputRef} />
      <button onClick={focusInput}>Focus</button>
    </>
  );
}
```



# useReducer

## What is useReducer?

It manages complex state logic.

Think of it as a more powerful version of `useState`.

### Syntax

``` jsx
const [state, dispatch] = useReducer(reducer, initialState);
```

### Example

``` jsx
function reducer(state, action) {
  switch (action.type) {
    case "increment":
      return { count: state.count + 1 };
    default:
      return state;
  }
}
```


# useCallback

## What is useCallback?

`useCallback` remembers (memoizes) a function so that it isn't recreated
on every render.

### Syntax

``` jsx
const memoizedFunction = useCallback(() => {
  // code
}, []);
```

### Why use it?

-   Improves performance
-   Prevents unnecessary re-renders
-   Useful when passing functions to child components



# useMemo

## What is useMemo?

`useMemo` remembers the result of an expensive calculation.

Instead of calculating again on every render, React reuses the previous
value.

### Syntax

``` jsx
const value = useMemo(() => {
  return expensiveCalculation();
}, []);
```

### Example

``` jsx
const square = useMemo(() => {
  return number * number;
}, [number]);
```


# Custom Hooks

## What are Custom Hooks?

A Custom Hook is a JavaScript function that starts with **use** and
contains other Hooks.

They help reuse logic between components.

### Example

``` jsx
import { useState } from "react";

function useCounter() {
  const [count, setCount] = useState(0);

  function increment() {
    setCount(count + 1);
  }

  return { count, increment };
}
```

Using the custom hook:

``` jsx
function App() {
  const { count, increment } = useCounter();

  return (
    <>
      <h2>{count}</h2>
      <button onClick={increment}>+</button>
    </>
  );
}
```


# Rules of Hooks

-   Always call Hooks at the top level.
-   Never call Hooks inside loops.
-   Never call Hooks inside conditions.
-   Only call Hooks inside React functional components or custom hooks.



# Best Practices

-   Use `useState` for simple state.
-   Use `useReducer` for complex state.
-   Use `useEffect` for API calls and side effects.
-   Use `useContext` to avoid prop drilling.
-   Use `useRef` for DOM access.
-   Use `useMemo` and `useCallback` only when they improve performance.
-   Create custom hooks to reuse logic.



# Quick Revision

  Hook          Purpose
  ------------- ---------------------------
  useState      Store state
  useEffect     Side effects
  useContext    Share data
  useRef        Access DOM / store values
  useReducer    Complex state
  useCallback   Memoize functions
  useMemo       Memoize values
  Custom Hook   Reuse logic



## Final Summary

By learning these Hooks, you can build modern React applications using
functional components without relying on class components. Understanding
when and why to use each Hook is an important skill for React interviews
and real-world projects.

