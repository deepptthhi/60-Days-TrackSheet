
## What is Middleware?

Middleware is a function that runs **between receiving a request and sending a response** in an Express application.

It acts as a bridge between the client request and the final route handler.

Middleware can:

- Execute code
- Read or modify the request (`req`)
- Read or modify the response (`res`)
- End the request-response cycle
- Pass control to the next middleware using `next()`


## Why Do We Need Middleware?

Imagine entering a company office.

Before meeting an employee, you pass through:

- Security Check
- Reception Desk
- Visitor Verification

Only after these steps are you allowed inside.

Middleware works in the same way. Every request passes through one or more middleware functions before reaching the actual route.

Benefits:

- Code reusability
- Better organization
- Authentication and authorization
- Request validation
- Logging requests
- Error handling


## Request Flow in Express

```text
Client Request
      │
      ▼
Middleware
      │
      ▼
Middleware
      │
      ▼
Route Handler
      │
      ▼
Response
```


## Middleware Function

Every middleware function receives three parameters.

```javascript
(req, res, next)
```

Where:

- `req` → Contains information about the incoming request.
- `res` → Used to send the response.
- `next()` → Passes control to the next middleware or route handler.

Example:

```javascript
app.use((req, res, next) => {
    console.log("Middleware Executed");
    next();
});
```

Output (when any request is made):

```text
Middleware Executed
```


## What Happens if next() is Not Called?

If a middleware neither sends a response nor calls `next()`, the request gets stuck.

```javascript
app.use((req, res, next) => {
    console.log("Request Received");
});
```

The browser will keep loading because Express doesn't know what to do next.

## Types of Middleware

### 1. Application Middleware

Runs for every request.

```javascript
app.use((req, res, next) => {
    console.log("Application Middleware");
    next();
});
```

Example:

```text
GET /
GET /about
POST /login

Application Middleware runs for all of them.
```


### 2. Route Middleware

Runs only for a specific route.

```javascript
app.get(
    "/profile",
    (req, res, next) => {
        console.log("Checking Profile");
        next();
    },
    (req, res) => {
        res.send("Profile Page");
    }
);
```

Output:

```text
Checking Profile
Profile Page
```


### 3. Built-in Middleware

Express provides some middleware by default.


## express.json()

Parses incoming JSON data.

```javascript
app.use(express.json());
```

Request:

```json
{
    "name": "Deepthi",
    "age": 22
}
```

Now we can access:

```javascript
console.log(req.body.name);
```

Output:

```text
Deepthi
```

## express.urlencoded()

Parses data submitted through HTML forms.

```javascript
app.use(express.urlencoded({ extended: true }));
```

Useful when handling form submissions.


## express.static()

Serves static files like:

- HTML
- CSS
- JavaScript
- Images
- Videos

```javascript
app.use(express.static("public"));
```

Folder Structure

```text
public/
│
├── style.css
├── logo.png
└── script.js
```

Browser:

```text
http://localhost:3000/logo.png
```

## Third-Party Middleware

Middleware created by other developers and installed using npm.

Examples:

- cors
- morgan
- helmet
- compression


## CORS Middleware

Install:

```bash
npm install cors
```

Usage:

```javascript
import cors from "cors";

app.use(cors());
```

Purpose:

Allows requests from different origins.

Example:

Frontend:

```text
http://localhost:5173
```

Backend:

```text
http://localhost:3000
```

Without CORS:

```text
Access blocked by browser
```


## Morgan Middleware

Install:

```bash
npm install morgan
```

Usage:

```javascript
import morgan from "morgan";

app.use(morgan("dev"));
```

Example Output:

```text
GET /users 200 15 ms
```

Morgan automatically logs incoming requests.


## Custom Middleware

You can create your own middleware.

```javascript
function logger(req, res, next) {
    console.log(req.method);
    console.log(req.url);

    next();
}

app.use(logger);
```

Output:

```text
GET
/users
```



## Authentication Middleware

Authentication middleware checks whether a user is allowed to access a route.

```javascript
function auth(req, res, next) {

    const token = req.headers.authorization;

    if (!token) {
        return res.status(401).json({
            message: "Unauthorized"
        });
    }

    next();
}
```

Using it:

```javascript
app.get("/admin", auth, (req, res) => {
    res.send("Welcome Admin");
});
```

## Multiple Middleware

Multiple middleware execute one after another.

```javascript
app.use((req, res, next) => {
    console.log("First");
    next();
});

app.use((req, res, next) => {
    console.log("Second");
    next();
});

app.get("/", (req, res) => {
    res.send("Home");
});
```

Output:

```text
First
Second
Home
```

## Middleware Execution Order

Express executes middleware in the same order they are registered.

```javascript
app.use(express.json());

app.use(logger);

app.use(auth);

app.get("/dashboard", dashboardHandler);
```

Execution:

```text
express.json()

↓

logger

↓

auth

↓

dashboardHandler
```

## Error-Handling Middleware

Error middleware has **four parameters**.

```javascript
app.use((err, req, res, next) => {

    res.status(500).json({
        error: err.message
    });

});
```

Example:

```javascript
app.get("/", (req, res) => {
    throw new Error("Something went wrong");
});
```

Response:

```json
{
    "error": "Something went wrong"
}
```


## Request Lifecycle

```text
Client
   │
   ▼
express.json()
   │
   ▼
Logger Middleware
   │
   ▼
Authentication Middleware
   │
   ▼
Validation Middleware
   │
   ▼
Route Handler
   │
   ▼
Response
```


## Best Practices

- Keep each middleware focused on a single task.
- Always call `next()` unless sending a response.
- Register middleware before defining routes.
- Put error-handling middleware at the end.
- Avoid writing very large middleware functions.
- Reuse middleware whenever possible.

## Common Interview Questions

### What is middleware?

Middleware is a function that executes during the request-response cycle and can process requests before they reach the route handler.



### Why is `next()` used?

`next()` tells Express to move to the next middleware or route handler.



### What happens if `next()` is not called?

The request remains pending unless a response is sent.



### Difference between `app.use()` and `app.get()`?

| app.use() | app.get() |
|------------|-----------|
| Used mainly for middleware | Handles only GET requests |
| Works for multiple HTTP methods | Runs only for GET |



### Difference between Application Middleware and Route Middleware?

| Application Middleware | Route Middleware |
|-------------------------|------------------|
| Runs globally | Runs for specific routes |
| Registered using `app.use()` | Registered with a route |



## Quick Revision

- Middleware runs between the request and response.
- Every middleware receives `req`, `res`, and `next()`.
- `next()` passes control to the next middleware.
- `express.json()` parses JSON data.
- `express.urlencoded()` parses form data.
- `express.static()` serves static files.
- CORS allows requests from different origins.
- Morgan logs HTTP requests.
- Custom middleware helps reuse logic.
- Authentication middleware protects routes.
- Error middleware has four parameters.
- Middleware executes in the order it is registered.