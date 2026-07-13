# Modern React Topics (Beyond the Basics)

These topics are commonly used in real-world React projects and are
frequently asked about in interviews.



# 1. React Project Folder Structure

A good folder structure makes projects easier to maintain.

    src/
    │
    ├── assets/
    ├── components/
    ├── pages/
    ├── hooks/
    ├── context/
    ├── services/
    ├── utils/
    ├── styles/
    ├── App.jsx
    └── main.jsx

### Why?

-   Easy to find files
-   Better organization
-   Scales well as the project grows



# 2. State Management

## What is State Management?

State management helps share and manage data across many components.

### Popular Libraries

-   React Context API (small apps)
-   Redux Toolkit (large apps)
-   Zustand (simple and lightweight)

### When to use Redux?

-   User authentication
-   Shopping cart
-   Dashboard data
-   Global settings



# 3. API Calls

React applications often fetch data from servers.

## Using fetch()

``` jsx
useEffect(() => {
  fetch("https://api.example.com/users")
    .then(res => res.json())
    .then(data => console.log(data));
}, []);
```

## Using Axios

Install:

``` bash
npm install axios
```

Example

``` jsx
import axios from "axios";

useEffect(() => {
  axios.get("/users")
       .then(res => console.log(res.data));
}, []);
```

Why Axios?

-   Cleaner syntax
-   Better error handling
-   Request interceptors
-   Automatic JSON parsing



# 4. React Query (TanStack Query)

React Query simplifies API data fetching.

Install

``` bash
npm install @tanstack/react-query
```

Features

-   Automatic caching
-   Background refetching
-   Loading state
-   Error handling

Instead of manually writing useEffect for every API call, React Query
manages server data efficiently.


# 5. Authentication

Authentication verifies a user's identity.

Common methods

-   Email & Password
-   Google Login
-   GitHub Login
-   JWT Authentication
-   Firebase Authentication

Typical Flow

    Login
     ↓
    Receive Token
     ↓
    Store Token
     ↓
    Send Token with API Requests



# 6. Performance Optimization

Large React apps can become slow.

Useful techniques

-   React.memo()
-   useMemo()
-   useCallback()
-   Lazy Loading
-   Code Splitting
-   Virtualization for long lists

Always optimize only after identifying a real performance issue.



# 7. Deployment

Deployment makes your app available online.

Popular platforms

-   Vercel
-   Netlify
-   GitHub Pages
-   Firebase Hosting

Typical Vite deployment

``` bash
npm run build
```

Upload the generated **dist** folder to your hosting platform.


# 8. Common React Interview Questions

### What is React?

A JavaScript library for building user interfaces.

### What is JSX?

HTML-like syntax inside JavaScript.

### Difference between Props and State?

Props - Passed from parent - Read-only

State - Managed inside component - Can change

### What is Virtual DOM?

A lightweight copy of the real DOM. React compares changes and updates
only the necessary elements, improving performance.

### What are Hooks?

Functions that allow functional components to use React features like
state and lifecycle.

### Why use Keys in Lists?

Keys help React identify items efficiently while rendering lists.

### What is Prop Drilling?

Passing props through multiple components unnecessarily. Context API can
help avoid this.

### Difference between useMemo and useCallback?

-   useMemo remembers a calculated value.
-   useCallback remembers a function.



# Quick Revision

  Topic                 Purpose
  --------------------- -------------------------
  Folder Structure      Organize project
  Redux/Zustand         Global state
  fetch/Axios           API calls
  React Query           Server state management
  Authentication        User login
  Performance           Faster UI
  Deployment            Host application
  Interview Questions   Revision



## Final Note

Learning React doesn't stop with components and hooks. Real-world
applications also involve API integration, authentication, state
management, performance optimization, and deployment. Mastering these
topics will make you much more confident while building projects and
facing technical interviews.
