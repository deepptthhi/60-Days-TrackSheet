# Day 24 - Learning Express.js Middleware

## What did I learn?

Today I spent time learning one of the core concepts of Express.js **middleware**. Yesterday I learned how to create routes and APIs, but today I finally understood what actually happens before a request reaches those routes.

At first, middleware felt like just another function that every tutorial seemed to use. But as I practiced, I realized it's much more than that. Middleware acts like a checkpoint where every request can be processed before it reaches the final route handler. Whether it's checking if a user is logged in, validating incoming data, parsing JSON, or simply logging requests, middleware is responsible for handling these tasks in an organized way.

One thing I really liked was how middleware helps keep the code clean. Instead of writing the same logic inside every route, I can create a middleware once and reuse it wherever it's needed. That made me understand why Express applications are easier to maintain even as they grow larger.

I also learned about Express's built-in middleware like **`express.json()`**, **`express.urlencoded()`**, and **`express.static()`**, which handle common tasks with just a single line of code. Along with that, I explored third-party middleware such as **CORS** and **Morgan**, and it became clear why they're used in almost every backend project.

By the end of today's learning, middleware no longer felt confusing. Instead, it became one of those concepts that made the overall request flow in Express much easier to understand.


## What challenges did I face?

The biggest challenge today was understanding the purpose of the **`next()`** function.

Initially, I knew I had to include it because every example used it, but I didn't really know why. After experimenting with my own code, I realized that if `next()` isn't called, Express doesn't know what to execute next, so the request simply stays pending.

I also found it a little confusing to differentiate between application middleware, route middleware, and error-handling middleware since they all looked quite similar. After writing a few examples and observing when each one was executed, the differences became much clearer.

Another thing I had to keep reminding myself was that middleware executes in the exact order it's registered. Once I visualized the request flow step by step, everything started making sense.


## What new concepts did I understand?

### Middleware

I learned that middleware sits between the client's request and the route handler, allowing the server to process requests before sending a response.

### The `next()` Function

I understood that `next()` tells Express to continue executing the next middleware or route handler. Without it, the request doesn't move forward.

### Built-in Middleware

Today I learned how middleware like `express.json()`, `express.urlencoded()`, and `express.static()` simplify common backend tasks and reduce the amount of code we need to write.

### Third-Party Middleware

I explored middleware packages like **CORS**, which allows communication between different origins, and **Morgan**, which automatically logs incoming HTTP requests.

### Custom Middleware

I also learned how to create my own middleware, making it easy to reuse common logic like logging, authentication, and request validation across multiple routes.


## What computer/software engineering fundamentals did I learn today?

Today's learning showed me that writing backend code isn't just about making things work, it's also about organizing the code in a way that's clean, reusable, and easy to maintain.

Middleware follows the principle of **separation of concerns**, where each middleware has a single responsibility. This keeps backend applications modular and makes them much easier to scale as new features are added.

I also realized why middleware is such an important part of backend development and why almost every Express application depends on it.


## What changed in my thinking?

Before today, I thought middleware was just another concept I needed to memorize to build Express applications.

After learning how it actually works, I realized it's one of the features that makes Express so powerful. Instead of repeating the same logic across multiple routes, middleware lets us write reusable code that automatically runs whenever it's needed.

The biggest realization for me was understanding that a request doesn't directly reach a route. There's an entire flow happening behind the scenes, and middleware is what controls and organizes that flow.

That completely changed the way I look at how backend applications process requests.


## Today's One Line Summary

> **"Today I learned that middleware is what keeps an Express application organized by processing every request before it reaches the actual route, making backend development much cleaner and easier to manage."**