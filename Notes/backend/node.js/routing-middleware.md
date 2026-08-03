

## Introduction

After learning the MVC architecture in Express.js, the next important concepts are **Routing** and **Middleware**. These two concepts form the backbone of every Express application.

Whenever a client sends a request to the server, Express needs to determine:

- Which URL was requested?
- Which HTTP method (GET, POST, etc.) was used?
- Which function should execute?
- Should anything happen before the request reaches the controller?

Routing answers **where** the request should go, while Middleware decides **what should happen before or after** the request is processed.

# What is Routing?

A **Route** is a combination of an HTTP method and a URL that tells Express which function should handle a request.

Think of routing like a receptionist in an office.

```
Customer
   ↓
Receptionist
   ↓
Correct Department
```

Similarly,

```
Client Request
      ↓
Express Router
      ↓
Controller Function
```

Example:

```javascript
app.get("/", (req, res) => {
    res.send("Welcome");
});
```

Whenever someone visits the homepage (`/`) using the **GET** method, Express executes the callback function.

# HTTP Methods

Different HTTP methods perform different operations.

| Method | Purpose |
|----------|-----------------------------|
| GET | Retrieve data |
| POST | Create new data |
| PUT | Replace existing data |
| PATCH | Update part of existing data |
| DELETE | Remove data |

Examples

```
GET /users
```

Returns all users.

```
POST /users
```

Creates a new user.

```
PUT /users/5
```

Replaces the details of user 5.

```
PATCH /users/5
```

Updates only selected fields.

```
DELETE /users/5
```

Deletes user 5.

# Basic Routing

```javascript
const express = require("express");

const app = express();

app.get("/", (req, res) => {
    res.send("Hello World");
});
```

### Explanation

- `app.get()` creates a GET route.
- `/` represents the homepage.
- `req` stores request information.
- `res` sends a response back to the client.

# Multiple Routes

```javascript
app.get("/", (req, res) => {
    res.send("Home");
});

app.get("/about", (req, res) => {
    res.send("About");
});

app.get("/contact", (req, res) => {
    res.send("Contact");
});
```

Each URL executes a different function.

# Route Parameters

Sometimes URLs contain dynamic values.

Example

```
/users/10
```

Here, **10** is dynamic.

Express captures it using `:`.

```javascript
app.get("/users/:id", (req, res) => {
    res.send(req.params.id);
});
```

Request

```
GET /users/10
```

Output

```
10
```

# Multiple Route Parameters

```javascript
app.get("/students/:name/:age", (req, res) => {
    res.send(req.params);
});
```

Request

```
/students/Deepthi/22
```

Output

```json
{
    "name": "Deepthi",
    "age": "22"
}
```

# Query Parameters

Query parameters appear after the `?` symbol.

Example

```
/search?product=laptop
```

Access them using

```javascript
req.query
```

Example

```javascript
app.get("/search", (req, res) => {
    res.send(req.query.product);
});
```

Request

```
/search?product=phone
```

Output

```
phone
```

# Request Body

POST and PUT requests usually send data inside the request body.

Example JSON

```json
{
    "name": "Deepthi",
    "age": 22
}
```

Enable JSON parsing.

```javascript
app.use(express.json());
```

Access the data.

```javascript
app.post("/users", (req, res) => {
    console.log(req.body);
});
```

# Response Methods

## res.send()

Sends text or HTML.

```javascript
res.send("Hello");
```

## res.json()

Sends JSON data.

```javascript
res.json({
    success: true
});
```

## res.status()

Sets an HTTP status code.

```javascript
res.status(404).send("Not Found");
```

## res.sendStatus()

Sets the status code and sends the default message.

```javascript
res.sendStatus(500);
```

# Express Router

Instead of writing all routes inside `app.js`, we organize them into separate files.

Project structure

```
routes/
    userRoutes.js
```

Example

```javascript
const express = require("express");

const router = express.Router();

router.get("/", (req, res) => {
    res.send("Users");
});

module.exports = router;
```

Import it inside `app.js`

```javascript
const userRoutes = require("./routes/userRoutes");

app.use("/users", userRoutes);
```

Now,

```
GET /users
```

automatically uses the router.

# What is Middleware?

Middleware is a function that executes **between receiving a request and sending the response**.

Flow

```
Client
   ↓
Middleware
   ↓
Controller
   ↓
Response
```

Middleware can

- Authenticate users
- Log requests
- Validate data
- Modify requests
- Handle errors

# Basic Middleware

```javascript
app.use((req, res, next) => {

    console.log("Request Received");

    next();

});
```

# What is next()?

`next()` tells Express to continue to the next middleware or route.

Without `next()`

```
Client
   ↓
Middleware
   ↓
Stops Here
```

With `next()`

```
Client
   ↓
Middleware
   ↓
Route
   ↓
Response
```

# Route-Specific Middleware

```javascript
function logger(req, res, next) {

    console.log("Logging Request");

    next();

}

app.get("/home", logger, (req, res) => {

    res.send("Welcome Home");

});
```

The middleware runs only for `/home`.

# Built-in Middleware

## JSON Middleware

```javascript
app.use(express.json());
```

Parses JSON request bodies.

## URL Encoded Middleware

```javascript
app.use(express.urlencoded({ extended: true }));
```

Reads HTML form data.

## Static Middleware

```javascript
app.use(express.static("public"));
```

Suppose the folder contains

```
public/
    logo.png
```

Open

```
http://localhost:3000/logo.png
```

to access the image.

# Custom Middleware Example

```javascript
function checkAge(req, res, next) {

    if (req.query.age >= 18) {

        next();

    } else {

        res.send("Access Denied");

    }

}

app.get("/movie", checkAge, (req, res) => {

    res.send("Enjoy the Movie");

});
```

Request

```
/movie?age=20
```

Output

```
Enjoy the Movie
```

Request

```
/movie?age=15
```

Output

```
Access Denied
```

# Error Handling Middleware

Error-handling middleware has four parameters.

```javascript
app.use((err, req, res, next) => {

    res.status(500).json({

        message: err.message

    });

});
```

Always place it **at the end** of your application.

# Express Request Lifecycle

```
Client
   │
   ▼
Incoming Request
   │
   ▼
Middleware
   │
   ▼
Router
   │
   ▼
Controller
   │
   ▼
Database
   │
   ▼
Controller
   │
   ▼
Response
   │
   ▼
Client
```

# Best Practices

- Keep routes simple and readable.
- Use `express.Router()` to organize routes.
- Keep business logic inside controllers.
- Use middleware for authentication and validation.
- Always call `next()` unless ending the request.
- Return proper HTTP status codes.
- Follow REST API naming conventions.

# Real-World Example (E-Commerce API)

```
GET /products
```

Returns all products.

```
GET /products/5
```

Returns product 5.

```
POST /products
```

Creates a new product.

```
PUT /products/5
```

Replaces product information.

```
PATCH /products/5
```

Updates selected fields.

```
DELETE /products/5
```

Deletes product 5.

Common middleware used in production:

- Authentication
- Authorization
- Request Logging
- Input Validation
- Rate Limiting
- Error Handling

# Summary

In this lesson, you learned:

- What routing is and why it is important.
- Different HTTP methods and their purposes.
- Route parameters using `req.params`.
- Query parameters using `req.query`.
- Reading request bodies using `req.body`.
- Sending responses with `res.send()`, `res.json()`, and `res.status()`.
- Organizing routes using `express.Router()`.
- What middleware is and where it fits in the request lifecycle.
- Using built-in middleware like `express.json()` and `express.static()`.
- Creating custom middleware.
- Handling errors using error-handling middleware.

Routing decides **where a request should go**, while middleware decides **what should happen before or after the request is processed**. Together, they form the foundation of scalable Express.js applications.