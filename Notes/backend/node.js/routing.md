

## What is Routing?

Routing is the process of defining how an Express server responds to different client requests.

A route is made up of:

- HTTP Method (GET, POST, PUT, DELETE, etc.)
- URL (Endpoint)
- Callback Function (Handler)

Example:

```javascript
app.get("/users", (req, res) => {
    res.send("All Users");
});
```

When a client sends a **GET** request to `/users`, Express executes the callback function.



## Why Do We Need Routing?

Without routing, every request would have to be handled in one file, making the application difficult to manage.

Routing helps us:

- Organize endpoints
- Improve code readability
- Separate different features
- Make applications scalable

Example:

```
/users
/products
/orders
/login
```

Each endpoint performs a different task.



## Express Router

Instead of defining every route in `server.js`, Express provides `Router()`.

Example:

```javascript
import express from "express";

const router = express.Router();

router.get("/", (req, res) => {
    res.send("All Products");
});

export default router;
```

Register the router:

```javascript
import productRoutes from "./routes/productRoutes.js";

app.use("/products", productRoutes);
```

Now visiting:

```
GET /products
```

will execute the router.



## Request Flow

```
Client Request
      │
      ▼
Route
      │
      ▼
Controller
      │
      ▼
Database
      │
      ▼
Response
```

# What is MVC?

MVC stands for:

- Model
- View
- Controller

It separates different responsibilities inside an application.

```
Routes
   │
   ▼
Controllers
   │
   ▼
Models
```

In backend APIs, the View is usually handled by frontend frameworks like React.



## Model

The Model represents application data.

Examples:

```
User
Product
Order
Employee
```

A model defines what information is stored.

Example:

```javascript
{
    name,
    email,
    password
}
```



## Controller

Controllers contain the business logic.

Instead of writing everything inside routes,

Bad:

```javascript
router.get("/", (req, res) => {
    // lots of logic
});
```

Good:

```javascript
export function getUsers(req, res) {
    res.send("Users");
}
```

Routes simply call the controller.




## Routes

Routes decide **which controller should execute**.

Example:

```javascript
router.get("/", getUsers);

router.post("/", createUser);

router.put("/:id", updateUser);

router.delete("/:id", deleteUser);
```

Routes should contain very little logic.



## Recommended Folder Structure

```
backend/

controllers/

models/

routes/

middleware/

config/

utils/

server.js
```

This structure is commonly used in professional Express applications.



## Route Parameters

Route parameters are dynamic values inside the URL.

Example:

```
GET /users/101
```

Access using:

```javascript
req.params.id
```

Output:

```
101
```


## Query Parameters

Query parameters are used for filtering or searching.

Example:

```
GET /products?category=Shoes
```

Access:

```javascript
req.query.category
```

Output:

```
Shoes
```



## Request Body

The request body contains data sent by the client.

Example:

```json
{
    "name": "Deepthi",
    "age": 22
}
```

Access:

```javascript
req.body
```

Before using `req.body`, enable JSON parsing.

```javascript
app.use(express.json());
```



## HTTP Methods

| Method | Purpose |
|----------|----------|
| GET | Retrieve data |
| POST | Create new data |
| PUT | Update existing data |
| PATCH | Partially update data |
| DELETE | Delete data |



## HTTP Status Codes

Example:

```javascript
res.status(200).json(data);
```

Common Status Codes:

| Code | Meaning |
|------|---------|
| 200 | OK |
| 201 | Created |
| 204 | No Content |
| 400 | Bad Request |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |
| 500 | Internal Server Error |



## REST API Naming

Good Examples

```
GET /users

GET /users/1

POST /users

PUT /users/1

DELETE /users/1
```

Avoid

```
/getUsers

/addUser

/deleteUser
```

REST APIs should use **resources (nouns)** instead of actions (verbs).



## Good API Response

Success

```json
{
    "success": true,
    "data": {
        "name": "Deepthi"
    }
}
```

Error

```json
{
    "success": false,
    "message": "User not found"
}
```

Keeping responses consistent makes frontend integration easier.



## Typical Request Lifecycle

```
Client
   │
   ▼
Route
   │
   ▼
Controller
   │
   ▼
Model
   │
   ▼
Database
   │
   ▼
Controller
   │
   ▼
Response
```



## Best Practices

- Keep routes small and clean.
- Write business logic inside controllers.
- Keep database operations inside models.
- Follow REST API conventions.
- Use meaningful HTTP status codes.
- Organize files into folders.
- Keep API responses consistent.
- Separate configuration and utility files.



## Common Interview Questions

### What is routing?

Routing defines how an Express application responds to client requests for different URLs and HTTP methods.



### What is Express Router?

Express Router is a mini Express application used to organize routes into separate files.



### What is MVC?

MVC stands for Model, View, and Controller. It separates application logic, data handling, and presentation for better maintainability.



### Why use controllers?

Controllers keep business logic separate from routes, making the code cleaner and easier to maintain.


### Difference between Route Parameters and Query Parameters?

| Route Parameters | Query Parameters |
|------------------|------------------|
| Part of the URL | Added after `?` |
| Used to identify a resource | Used for filtering/searching |
| `req.params` | `req.query` |

Example:

```
/users/10
```

vs

```
/users?country=India
```



## Quick Revision

- Routing maps URLs to specific functions.
- `express.Router()` organizes routes into separate files.
- MVC = Model + View + Controller.
- Models represent application data.
- Controllers contain business logic.
- Routes connect requests to controllers.
- `req.params` reads route parameters.
- `req.query` reads query parameters.
- `req.body` reads request data.
- Always enable `express.json()` for JSON requests.
- Use correct HTTP methods.
- Return proper HTTP status codes.
- Follow REST API naming conventions.
- Keep routes thin and controllers focused.