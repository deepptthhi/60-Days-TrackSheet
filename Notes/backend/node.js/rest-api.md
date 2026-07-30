

## What is an API?

API stands for **Application Programming Interface**.

It allows two applications to communicate with each other.

Example:
Frontend → API → Backend → Database

When you open Instagram:
- Frontend asks for posts.
- Backend fetches posts from the database.
- Backend sends the data back as JSON.
- Frontend displays it.

The API is the bridge between frontend and backend.

## What is REST?

REST stands for Representational State Transfer.

It is a standard way of designing APIs.

REST APIs use:
- URLs
- HTTP Methods
- Status Codes
- JSON

Example:

GET /users

returns

[
  {
    "id": 1,
    "name": "Deepthi"
  }
]

## HTTP Methods

### GET

Used to fetch data.

Example:

GET /users

Returns all users.

### POST

Used to create new data.

Example:

POST /users

Body

{
  "name": "Deepthi"
}

Creates a new user.

### PUT

Updates an entire resource.

Example:

PUT /users/1

Updates all details of user 1.

### PATCH

Updates only specific fields.

Example:

PATCH /users/1

{
  "age": 22
}

Only the age changes.

### DELETE

Deletes data.

Example:

DELETE /users/1

Deletes user 1.

## CRUD Operations

CRUD means:

- Create
- Read
- Update
- Delete

Mapping:

- Create → POST
- Read → GET
- Update → PUT/PATCH
- Delete → DELETE

## API Endpoints

Endpoints are URLs exposed by the backend.

Examples:

GET /products

GET /products/5

POST /products

DELETE /products/5

Each endpoint performs one specific task.

## Route Parameters

Route parameters are dynamic values inside the URL.

Example:

```javascript
app.get("/users/:id", (req, res) => {
    console.log(req.params.id);
});
```

Request:

/users/15

Output:

15

`req.params` stores values from the URL.

## Query Parameters

Query parameters are used for filtering, searching, sorting, or pagination.

Example:

/products?category=mobile

Access it using:

```javascript
req.query.category
```

Output:

mobile

Another example:

/users?page=2&limit=10

## Request Body

The request body contains data sent by the client.

Example:

POST /users

```json
{
  "name": "Deepthi",
  "age": 22
}
```

Access it using:

```javascript
req.body
```

Enable it with:

```javascript
app.use(express.json());
```

## Response

The backend sends responses using:

```javascript
res.send("Hello");
```

For JSON responses:

```javascript
res.json({
    name: "Deepthi"
});
```

JSON responses are the standard for REST APIs.

## HTTP Status Codes

| Code | Meaning |
|------|----------|
| 200 | Success |
| 201 | Resource Created |
| 400 | Bad Request |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |
| 500 | Internal Server Error |

Example:

```javascript
res.status(201).json(user);
```

## Standard REST API Routes

GET /users

Returns all users.

GET /users/:id

Returns one user.

POST /users

Creates a new user.

PUT /users/:id

Updates the entire user.

PATCH /users/:id

Updates selected fields.

DELETE /users/:id

Deletes the user.

## Example Express REST API

```javascript
const express = require("express");

const app = express();

app.use(express.json());

let users = [];

app.get("/users", (req, res) => {
    res.json(users);
});

app.post("/users", (req, res) => {
    users.push(req.body);
    res.status(201).json(req.body);
});

app.listen(3000);
```

## Request Flow

Client

↓

HTTP Request

↓

Express Route

↓

Business Logic

↓

Database

↓

HTTP Response

↓

Client

## API Testing Tools

You can test APIs using:

- Postman
- Thunder Client (VS Code)
- curl

Example:

```bash
curl http://localhost:3000/users
```

## JSON

JSON stands for JavaScript Object Notation.

Example:

```json
{
  "name": "Deepthi",
  "city": "Bangalore"
}
```

Rules:

- Keys must use double quotes.
- Supports strings, numbers, booleans, arrays, objects, and null.

## Middleware Review

Middleware runs before the route handler.

Example:

```javascript
app.use(express.json());
```

Purpose:

- Reads incoming JSON.
- Converts it into a JavaScript object.
- Makes it available through `req.body`.

Without this middleware, `req.body` will be `undefined`.

## Route Parameters vs Query Parameters

### Route Parameters

Example:

/users/10

Access:

```javascript
req.params.id
```

Used to identify a specific resource.

### Query Parameters

Example:

/users?page=2

Access:

```javascript
req.query.page
```

Used for filtering, searching, sorting, and pagination.

## Best Practices

- Use nouns instead of verbs.
- Return proper HTTP status codes.
- Return JSON responses.
- Keep URLs meaningful.
- Validate incoming data.
- Handle errors properly.

Good:

/users

/products

/orders

Bad:

/getUsers

/createUser

## Interview Questions

### What is a REST API?

A REST API is a backend service that allows applications to communicate using HTTP methods while following REST principles.

### Difference between GET and POST?

GET retrieves data.

POST creates new data.

### Difference between PUT and PATCH?

PUT updates the complete resource.

PATCH updates only selected fields.

### Difference between req.params and req.query?

`req.params` comes from the URL path.

`req.query` comes after the `?` in the URL.

### Why do we use express.json()?

It converts incoming JSON into JavaScript objects so that we can access it using `req.body`.

### What is CRUD?

CRUD stands for Create, Read, Update, and Delete.

### Why is JSON used?

Because it is lightweight, easy to read, and supported by almost every programming language.

### Which status code is used after creating a resource?

201 Created.

### Which tools are commonly used for API testing?

Postman, Thunder Client, and curl.

