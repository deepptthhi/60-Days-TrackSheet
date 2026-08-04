#  Express.js REST APIs & CRUD Operations

## Introduction

After learning about **Routing** and **Middleware**, the next step is understanding how backend applications communicate with frontend applications through **REST APIs**.

Today, we will learn:

- What an API is
- What REST means
- REST principles
- CRUD operations
- Building REST APIs using Express
- HTTP Status Codes
- Testing APIs using Postman
- REST API Best Practices

A REST API allows different applications (frontend, mobile apps, or other servers) to communicate with the backend using HTTP requests.

# What is an API?

API stands for **Application Programming Interface**.

An API acts as a bridge between two applications.

Example:

```
Frontend
     │
     ▼
REST API
     │
     ▼
Backend
     │
     ▼
Database
```

Example:

A shopping website requests product information.

```
GET /products
```

The API retrieves data from the database and sends it back to the frontend.

# What is REST?

REST stands for **Representational State Transfer**.

It is a set of architectural principles used for designing web APIs.

REST APIs:

- Use HTTP methods
- Use URLs to identify resources
- Are stateless
- Return data (usually JSON)

Example:

```
GET /users
```

Returns all users.

```
POST /users
```

Creates a new user.

# REST Principles

## Client-Server Architecture

The client sends requests.

The server processes requests and sends responses.

```
Client

↓

Server

↓

Response
```

---

## Stateless

Each request contains all the information required.

The server does not remember previous requests.

Example:

```
GET /profile
Authorization Token
```

Every request must send its own authentication token.

---

## Resource-Based URLs

Resources are identified using nouns.

Good

```
/users
/products
/orders
```

Bad

```
/getUsers
/createUser
/deleteProduct
```

# CRUD Operations

CRUD represents the four basic database operations.

| Operation | HTTP Method | Example |
|------------|-------------|----------|
| Create | POST | POST /users |
| Read | GET | GET /users |
| Update | PUT/PATCH | PUT /users/1 |
| Delete | DELETE | DELETE /users/1 |

# Creating a REST API

Create an Express server.

```javascript
const express = require("express");

const app = express();

app.use(express.json());

app.listen(3000);
```

# GET Request

Retrieve all users.

```javascript
app.get("/users", (req, res) => {

    res.json([
        {
            id:1,
            name:"Deepthi"
        }
    ]);

});
```

Output

```json
[
    {
        "id":1,
        "name":"Deepthi"
    }
]
```

# POST Request

Create a new user.

```javascript
app.post("/users", (req, res) => {

    const user = req.body;

    res.status(201).json(user);

});
```

Request

```json
{
    "name":"Rahul"
}
```

Response

```json
{
    "name":"Rahul"
}
```

# PUT Request

Replace an existing resource.

```javascript
app.put("/users/:id",(req,res)=>{

    res.send("User Updated");

});
```

# PATCH Request

Update specific fields.

```javascript
app.patch("/users/:id",(req,res)=>{

    res.send("User Partially Updated");

});
```

# DELETE Request

Delete a resource.

```javascript
app.delete("/users/:id",(req,res)=>{

    res.send("User Deleted");

});
```

# HTTP Status Codes

Status codes tell the client whether a request succeeded or failed.

| Code | Meaning |
|------|-----------|
| 200 | OK |
| 201 | Created |
| 204 | No Content |
| 400 | Bad Request |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |
| 500 | Internal Server Error |

Example

```javascript
res.status(201).json(user);
```

# Request and Response

Client Request

```http
POST /users
Content-Type: application/json

{
    "name":"Deepthi"
}
```

Server Response

```http
HTTP/1.1 201 Created

{
    "name":"Deepthi"
}
```

# JSON

JSON stands for **JavaScript Object Notation**.

Example

```json
{
    "id":1,
    "name":"Deepthi",
    "age":22
}
```

JSON is lightweight and easy for applications to exchange data.

# REST API Folder Structure

```
project/

│

├── app.js

├── routes/

│      users.js

├── controllers/

│      userController.js

├── models/

│      userModel.js

├── middleware/

├── config/

└── package.json
```

# Testing APIs Using Postman

Postman allows developers to test APIs without building a frontend.

Example:

```
GET http://localhost:3000/users
```

You can:

- Send GET requests
- Send POST requests
- Send JSON data
- View responses
- Check status codes
- Debug APIs

# REST API Best Practices

- Use nouns instead of verbs in URLs.
- Return appropriate HTTP status codes.
- Validate incoming request data.
- Keep endpoints simple and meaningful.
- Return JSON responses.
- Use proper error messages.
- Separate routes, controllers, and models.
- Follow REST naming conventions.

# Real-World Example

Imagine an Online Shopping Application.

Get all products

```
GET /products
```

Get one product

```
GET /products/10
```

Create product

```
POST /products
```

Update product

```
PUT /products/10
```

Update product price

```
PATCH /products/10
```

Delete product

```
DELETE /products/10
```

# Request Lifecycle

```
Frontend

↓

REST API

↓

Middleware

↓

Router

↓

Controller

↓

Database

↓

Controller

↓

JSON Response

↓

Frontend
```

# Summary

Today, you learned:

- What an API is.
- What REST means.
- REST architectural principles.
- CRUD operations.
- Creating REST APIs in Express.
- GET, POST, PUT, PATCH, and DELETE requests.
- HTTP status codes.
- Sending and receiving JSON.
- Testing APIs using Postman.
- REST API best practices.

REST APIs are the foundation of modern backend development. Almost every web application, mobile application, and cloud service communicates through REST APIs, making this one of the most essential concepts for every backend developer.