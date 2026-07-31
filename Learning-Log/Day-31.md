# Day 31 - Media.net SRE Preparation | Learning Express.js Routing & Middleware

## What did I learn?

Today I continued my preparation for the **Media.net SRE interview** by learning **Express.js Routing and Middleware**. After understanding REST APIs in the previous session, today I learned how Express actually processes incoming requests and sends responses back to the client. This helped me understand what happens internally whenever someone accesses an API endpoint.

The first thing I learned was what **Express.js** really is. Although I had already used Express for creating APIs, I never fully understood why it is preferred over Node.js's built-in HTTP module. Today I realized that Express provides a much simpler and cleaner way to build web servers by handling routing, requests, responses, and middleware with very little code.

I then explored **routing** in more detail. Earlier, I knew how to create routes, but today I understood that routing is responsible for deciding which piece of code should execute for a particular URL and HTTP method. This made me realize that every request made by the client is matched to a specific route before any business logic is executed.

Another important concept I learned was the difference between the **Request (`req`)** and **Response (`res`)** objects. I understood that the request object contains everything sent by the client, such as parameters, query strings, headers, and request body, while the response object is responsible for sending data back to the client. This made the request-response cycle much clearer.

The biggest topic I learned today was **Middleware**. Initially, middleware seemed confusing because it runs before the route handler, and I couldn't understand why it was necessary. After practicing examples, I realized that middleware acts as an intermediate layer that can perform tasks like logging requests, parsing JSON, authenticating users, and validating incoming data before the request reaches the actual route.

I also learned the importance of the **`next()`** function. Earlier, I simply copied it from examples without knowing its purpose. Today I understood that calling `next()` tells Express to continue processing the request by moving to the next middleware or the route handler. Without calling `next()`, the request stops and the client never receives a response.

Another useful concept I learned was **built-in middleware**, especially `express.json()`. Although I had been using it in previous projects, I finally understood that it converts incoming JSON data into JavaScript objects, allowing the backend to access the data through `req.body`.

Towards the end, I created a simple Express application that used multiple routes and middleware. Watching requests pass through middleware before reaching the route handler helped me visualize the complete lifecycle of an incoming request. This practical implementation made the entire execution flow much easier to understand.

By the end of today's learning, I realized that middleware is one of the most powerful features of Express because almost every real-world backend application uses it for logging, authentication, validation, security, and error handling. Understanding this execution flow also gave me a better idea of how production backend systems work.

## What challenges did I face?

The biggest challenge today was understanding how middleware executes before the route handler. Initially, I couldn't visualize why multiple functions were executed for a single request. After tracing the execution step by step, I understood how Express processes middleware sequentially.

Another challenge was understanding the purpose of the `next()` function. At first, it looked like just another function call, but after experimenting with and without it, I realized that it controls the entire middleware execution flow.

I also found it slightly confusing to differentiate between application-level middleware and route-level middleware. After implementing both, I understood when each one should be used.

## What new concepts did I understand?

### Express.js

I learned that Express.js is a lightweight framework that simplifies building web servers and REST APIs using Node.js.

### Routing

I understood that routing maps incoming HTTP requests to the correct handler based on the URL and HTTP method.

### Request Object (`req`)

I learned that the request object contains information sent by the client, including parameters, query strings, headers, and request body.

### Response Object (`res`)

I understood that the response object is used to send data, JSON, and status codes back to the client.

### Middleware

I learned that middleware executes before the route handler and is used for logging, authentication, validation, parsing requests, and many other common tasks.

### next()

I understood that `next()` allows Express to continue executing the next middleware or the final route handler.

### express.json()

I learned that `express.json()` converts incoming JSON data into JavaScript objects so that it can be accessed using `req.body`.

### Route Handler

I understood that the route handler contains the actual business logic that executes after all middleware has finished.

## What computer/software engineering fundamentals did I learn today?

Today's learning helped me understand that backend applications don't directly execute route handlers whenever a request arrives. Instead, every request passes through multiple layers of middleware before reaching the business logic. This layered architecture makes applications easier to maintain, secure, and scale.

I also realized that middleware promotes code reusability because common functionality like authentication, logging, and validation can be written once and reused across multiple routes instead of repeating the same code everywhere.

Another important takeaway was understanding the complete request lifecycle in an Express application, which is essential for debugging backend services and building production-ready APIs.

## What changed in my thinking?

Before today, I thought middleware was simply another function used in Express applications.

After today's learning, I realized that middleware forms the backbone of most backend applications. It controls how requests are processed, validated, authenticated, and logged before reaching the actual business logic.

The biggest realization for me today was that writing backend applications isn't only about creating routes—it's about building a structured request-processing pipeline that makes applications more secure, organized, and maintainable.

## Today's One Line Summary

> **"Today I learned how Express.js processes requests using routing and middleware, helping me understand the complete lifecycle of a backend request before it reaches the application logic."**