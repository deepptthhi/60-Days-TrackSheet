# Day 25 - Learning Express.js Routing, MVC Architecture & REST API Best Practices

## What did I learn?

Today felt like the day I started understanding how backend projects are actually built in the real world. Until now, I had been creating routes and APIs, but everything was inside one or two files. Today I learned why developers don't keep projects that way as they grow.

The biggest thing I learned was the **MVC architecture**. At first, it sounded like just another pattern to memorize, but once I understood that each part has its own responsibility, it all started making sense. Routes simply receive requests, controllers handle the logic, and models deal with the data. Keeping these separate makes the project much cleaner and easier to work on.

I also learned how **Express Router** helps organize routes into different files instead of filling `server.js` with hundreds of lines of code. That made me realize why project structure becomes just as important as writing the code itself.

Along the way, I explored **route parameters**, **query parameters**, **request bodies**, proper **HTTP methods**, and **status codes**. I also learned why REST APIs follow certain naming conventions and how those standards make APIs easier for everyone to understand.

By the end of today's learning, I felt like I wasn't just building APIs anymore—I was learning how to build backend applications the way professional developers do.

## What challenges did I face?

The biggest challenge today was understanding the difference between **routes** and **controllers**.

Initially, they both looked like places where code was written, so I couldn't understand why we needed separate files for them. After trying a few examples, I realized that routes are only responsible for deciding where a request should go, while controllers contain the actual logic that performs the work.

I also found myself getting confused between **route parameters**, **query parameters**, and **request bodies**. Since all of them send information to the server, it took me a little time to understand when each one should be used. Once I started comparing examples side by side, the differences became much clearer.

Another small challenge was getting used to REST API naming. I naturally wanted to write endpoints like `/getUsers`, but I learned that using resource names like `/users` is the standard approach and makes APIs much more consistent.

## What new concepts did I understand?

### Express Routing

I learned that routing connects a client's request to the correct function in the application. Every route is defined using an HTTP method and a URL.

### Express Router

I understood how `express.Router()` helps split routes into different files, making applications much cleaner and easier to maintain.

### MVC Architecture

Today I finally understood why developers use the MVC pattern. It separates responsibilities so that routes handle requests, controllers contain business logic, and models represent the application's data.

### Route Parameters

I learned that route parameters are used when identifying a specific resource, such as fetching a user using their ID.

### Query Parameters

I understood that query parameters are mainly used for searching, filtering, and sorting data without changing the main route.

### REST API Best Practices

I learned why using the correct HTTP methods, meaningful status codes, and resource based endpoint names makes APIs easier to understand and follow.

## What computer/software engineering fundamentals did I learn today?

Today's learning showed me that writing backend code isn't only about making an API work. It's also about organizing the project so that anyone can understand, maintain, and extend it in the future.

I saw another example of **separation of concerns**, where every part of the application has a single responsibility instead of trying to do everything in one place. This makes debugging easier, reduces code duplication, and helps projects scale as they become larger.

I also realized that following REST standards isn't just a best practice, it's something that allows different developers and applications to communicate in a consistent way.

## What changed in my thinking?

Before today, I thought organizing a project into routes, controllers, and models was mostly about keeping files neat.

After learning the MVC architecture, I realized it's much more than that. It's about making applications easier to build, debug, and improve over time. As projects grow, having a proper structure becomes just as important as writing the actual code.

The biggest realization for me was understanding that good backend development isn't just about solving the problem, it's also about solving it in a way that stays clean and manageable even months later. That changed how I look at building backend applications.

## Today's One Line Summary

> **"Today I learned that a well structured backend is just as important as working code, and using routing, MVC architecture, and REST principles makes applications much cleaner, easier to maintain, and ready to grow."**