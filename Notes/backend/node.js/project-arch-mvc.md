# Express Project Architecture (MVC)

## Introduction

As backend applications grow, managing all the code inside a single `server.js` or `app.js` file becomes increasingly difficult. While this approach may work for small applications, it quickly becomes hard to read, debug, and maintain as new features are added.

A well-organized project structure helps developers separate different responsibilities into dedicated files and folders. This improves code readability, promotes reusability, and makes collaboration easier when working in teams.

One of the most commonly used architectural patterns for backend development is the **MVC (Model-View-Controller)** architecture.

## Why Do We Need a Proper Project Structure?

Imagine building a simple application that initially supports only user registration and login.

As the project grows, you start adding:

- User Profiles
- Authentication
- Products
- Orders
- Payments
- Notifications
- Reviews
- Admin Dashboard

If every route, database query, middleware, and helper function is written inside one file, the application becomes difficult to understand and maintain.

A proper project structure helps by:

- Separating different responsibilities
- Improving readability
- Making debugging easier
- Encouraging code reuse
- Supporting scalability
- Allowing multiple developers to work independently

## What is MVC?

MVC stands for:

- **Model**
- **View**
- **Controller**

It is a software architecture pattern that separates an application into different layers, where each layer has a specific responsibility.

Although Express.js does not enforce MVC, it is widely adopted because it keeps applications organized and maintainable.

```
Client
   │
   ▼
Routes
   │
   ▼
Controller
   │
   ▼
Service (Optional)
   │
   ▼
Model
   │
   ▼
Database
```

Each layer focuses on a single responsibility, making the application easier to extend and maintain.

## Understanding the MVC Components

### Model

The Model represents the application's data and business entities.

Its responsibilities include:

- Defining database schemas
- Performing database operations
- Managing relationships between collections
- Validating stored data

Example using Mongoose:

```javascript
const mongoose = require("mongoose");

const userSchema = new mongoose.Schema({
    name: String,
    email: String,
    age: Number
});

module.exports = mongoose.model("User", userSchema);
```

The Model communicates directly with the database.

### View

In traditional MVC frameworks, the View is responsible for displaying information to users.

However, in REST API development, there is usually no HTML view.

Instead, Express APIs return JSON responses.

Example:

```javascript
res.json({
    message: "User created successfully"
});
```

In modern web applications, the frontend (React, Angular, Vue) acts as the View.

### Controller

The Controller acts as the bridge between incoming requests and business logic.

Its responsibilities include:

- Receiving requests
- Calling services or models
- Processing results
- Returning responses

Example:

```javascript
exports.getUsers = async (req, res) => {
    const users = await User.find();

    res.json(users);
};
```

Controllers should remain lightweight and avoid containing large amounts of business logic.

## Beyond MVC: The Service Layer

Many production applications introduce another layer called the **Service Layer**.

Instead of writing business logic inside controllers, controllers delegate that work to services.

```
Request
   │
Routes
   │
Controller
   │
Service
   │
Model
   │
Database
```

Example:

```javascript
async function createUser(userData) {
    return await User.create(userData);
}
```

Advantages:

- Cleaner controllers
- Better code reuse
- Easier testing
- Separation of business logic

## Recommended Folder Structure

```
project/

├── src/
│
├── controllers/
│
├── routes/
│
├── models/
│
├── middleware/
│
├── services/
│
├── validators/
│
├── config/
│
├── utils/
│
├── app.js
│
├── server.js
│
├── package.json
│
└── .env
```

Each folder serves a dedicated purpose.

## Routes

Routes define the application's API endpoints.

Example:

```javascript
router.get("/users", userController.getUsers);
```

Routes should remain simple and delegate work to controllers.

## Controllers

Controllers receive requests and send responses.

Example:

```javascript
exports.createUser = async (req, res) => {

    const user = await userService.create(req.body);

    res.status(201).json(user);

};
```

Controllers should not contain database queries whenever possible.

## Models

Models interact directly with the database.

Responsibilities include:

- Creating records
- Updating records
- Deleting records
- Querying data

They should never contain request or response logic.

## Middleware

Middleware executes before controllers.

Examples include:

- Authentication
- Logging
- Validation
- Error Handling

Middleware helps remove repeated code from controllers.

## Services

Services contain business logic.

Examples:

- Calculating order totals
- Sending emails
- Processing payments
- Applying discounts

This layer keeps controllers focused only on handling HTTP requests.

## Validators

Validation ensures incoming data is correct before processing.

Example:

```javascript
if (!req.body.email) {

    return res.status(400).json({
        message: "Email is required"
    });

}
```

Large applications typically use:

- express-validator
- Joi
- Zod

## Utilities

The `utils` folder contains reusable helper functions.

Examples:

- Date formatting
- Password hashing
- Token generation
- Email formatting

Utilities should not depend on request or response objects.

## Configuration

Configuration files manage application settings.

Examples:

- Database URLs
- JWT Secret
- API Keys
- SMTP Configuration

Keeping configuration separate improves security and flexibility.

## Request Lifecycle

A typical request follows this flow:

```
Client

↓

Route

↓

Middleware

↓

Controller

↓

Service

↓

Model

↓

Database

↓

Response
```

Understanding this flow makes debugging backend applications much easier.

## Separation of Concerns

Each component should focus on only one responsibility.

| Layer | Responsibility |
|--------|----------------|
| Routes | Define API endpoints |
| Middleware | Process incoming requests |
| Controllers | Handle request and response |
| Services | Business logic |
| Models | Database interaction |
| Utilities | Helper functions |
| Config | Application configuration |

This principle is called **Separation of Concerns**, one of the most important software engineering practices.

## Best Practices

- Keep controllers small.
- Move business logic into services.
- Validate all incoming requests.
- Use middleware for reusable functionality.
- Store secrets in environment variables.
- Follow consistent folder naming.
- Keep helper functions inside `utils`.

## Common Mistakes

- Writing everything inside `server.js`
- Putting database queries inside routes
- Mixing business logic with controllers
- Hardcoding secrets
- Repeating validation code
- Ignoring folder organization

## Real-World Example

Consider an e-commerce website.

When a customer places an order:

1. The request reaches the Route.
2. Authentication Middleware verifies the user.
3. The Controller receives the request.
4. The Service calculates the order total.
5. The Model stores the order in MongoDB.
6. The Controller sends a success response.

Each layer performs only its assigned responsibility, making the application easier to maintain and scale.

## Interview Questions

### Why is MVC used?

MVC separates responsibilities, making applications modular, scalable, and easier to maintain.

### Why shouldn't business logic be written inside controllers?

Controllers should only coordinate requests and responses. Business logic belongs in services because it is reusable and easier to test.

### Why are routes kept simple?

Routes only define API endpoints. Keeping them simple improves readability and prevents duplication.

### What is Separation of Concerns?

It is the principle of dividing an application into independent layers where each layer has a single responsibility.

## Summary

A well-structured project architecture is essential for building production-ready backend applications. By organizing code into routes, controllers, services, models, middleware, and utilities, developers can create applications that are easier to understand, maintain, and scale. While small projects may work with a single file, adopting an MVC-based architecture early prepares applications for future growth and team collaboration.