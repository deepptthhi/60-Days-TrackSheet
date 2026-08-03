# Day 34 - Learning Express.js Routing & Middleware

## What did I learn?

Today, I learned one of the most fundamental concepts in backend development using Express.js **Routing and Middleware**. Until now, I knew how to create a basic Express server and organize projects using the MVC architecture. However, I wasn't completely sure how incoming requests actually reached the correct function or how developers performed tasks like authentication, validation, or logging before processing a request. Today's learning helped me understand the complete request flow inside an Express application.

Yesterday, I learned how Express projects are structured using the MVC architecture. That gave me an understanding of how to separate controllers, models, and routes into different folders. Today, I built on that knowledge by learning how routes connect client requests to controllers and how middleware sits in between to process requests before they reach the application's business logic.

The first concept I understood today was **routing**. I learned that routing is the mechanism that tells Express which function should execute when a client sends a request to a specific URL using a particular HTTP method. Instead of writing one large function to handle every request, developers define individual routes that map requests to the appropriate controller. This makes backend applications much more organized and easier to maintain.

I then explored the different **HTTP methods** used while creating APIs. Although I had seen methods like GET and POST before, today I understood their actual purpose. GET is used to retrieve data, POST creates new resources, PUT replaces existing resources, PATCH updates specific fields, and DELETE removes resources. Understanding these methods helped me see how REST APIs are designed using standardized request types.

Another important concept I learned was **route parameters**. Earlier, I thought a separate route was required for every user or product. Today I realized that Express allows developers to create dynamic routes using parameters such as `:id`. This enables a single route to handle requests for multiple resources while retrieving the dynamic value using `req.params`.

I also learned about **query parameters**. I understood that query strings provide additional information to a request without changing the route itself. They are commonly used for searching, filtering, sorting, and pagination. Express makes these values available through the `req.query` object, making it easy to process user inputs from the URL.

Another concept I understood today was the **request body**. I learned that data sent by clients in POST, PUT, or PATCH requests is stored inside the request body and can be accessed using `req.body`. Since Express cannot read JSON data automatically, I also learned the purpose of using `express.json()` middleware to parse incoming JSON requests.

I also explored different **response methods** provided by Express. Instead of always using `res.send()`, I learned when to use methods such as `res.json()`, `res.status()`, and `res.sendStatus()`. This helped me understand how backend applications communicate meaningful responses and HTTP status codes back to the client.

One of the most valuable concepts I learned today was **Express Router**. Earlier, I would write every route inside a single `app.js` file. Today I understood why larger applications separate routes into dedicated files using `express.Router()`. This keeps projects modular, improves readability, and makes it easier to manage different resources such as users, products, and orders.

The biggest topic I learned today was **Middleware**. Initially, I thought middleware was just another function. After studying the request lifecycle, I realized that middleware acts as an intermediate layer between the client request and the route handler. Middleware can inspect, modify, validate, or even block requests before they reach the controller.

I also learned the importance of the **next()** function. At first, I did not understand why middleware required another function call. Today I realized that without calling `next()`, Express stops processing the request, preventing it from reaching the intended route handler. This helped me understand how multiple middleware functions execute sequentially.

Towards the end of today's learning, I explored **built-in middleware** provided by Express, such as `express.json()`, `express.urlencoded()`, and `express.static()`. I also learned how developers create custom middleware for authentication, request validation, logging, and other reusable functionality. Finally, I understood how **error-handling middleware** allows applications to manage unexpected errors consistently instead of crashing.

By the end of today's learning, I realized that routing and middleware form the core of every Express application. Routing determines where a request should go, while middleware controls how that request is processed before and after reaching the controller. Together, they make backend applications modular, secure, scalable, and easier to maintain.

## What challenges did I face?

The biggest challenge today was understanding the difference between **routing** and **middleware**. Initially, both seemed to perform similar tasks because they are involved in handling requests. After studying the request lifecycle, I realized that routing determines which controller should execute, whereas middleware performs additional processing before or after the request reaches the controller.

Another challenge was understanding the purpose of the **next()** function. At first, it seemed unnecessary because middleware itself was already executing. Once I understood that Express processes middleware sequentially and requires `next()` to continue the request flow, the concept became much clearer.

I also found it slightly confusing to differentiate between **route parameters**, **query parameters**, and the **request body**. After practicing multiple examples, I understood that route parameters identify resources, query parameters provide optional filtering information, and the request body carries data submitted by the client.

## What new concepts did I understand?

### Routing

I learned that routing maps HTTP requests to specific controller functions based on the request URL and HTTP method.

### HTTP Methods

I understood the purpose of GET, POST, PUT, PATCH, and DELETE methods and how they are used to design RESTful APIs.

### Route Parameters

I learned how dynamic URLs use parameters such as `:id` and how Express retrieves them through `req.params`.

### Query Parameters

I understood that query parameters provide additional request information such as search filters and pagination, and they can be accessed using `req.query`.

### Request Body

I learned that data sent in POST, PUT, and PATCH requests is stored inside `req.body` after parsing it with `express.json()`.

### Express Router

I understood that `express.Router()` allows developers to organize routes into separate modules, making applications cleaner and more scalable.

### Middleware

I learned that middleware executes before or after route handlers to perform tasks like logging, validation, authentication, and request processing.

### next()

I understood that `next()` passes control to the next middleware or route handler, allowing Express to continue processing the request.

### Error Handling Middleware

I learned how centralized error-handling middleware improves application reliability by managing errors consistently across the application.

## What computer/software engineering fundamentals did I learn today?

Today's learning helped me understand one of the most important principles in backend software engineering—**separating request processing from business logic**. Instead of placing validation, logging, and authentication inside controllers, middleware allows these responsibilities to be handled independently, making the application more modular and maintainable.

I also realized that RESTful backend applications rely on standardized HTTP methods and routing conventions to communicate with clients efficiently. This consistency improves readability, scalability, and collaboration among developers.

Another important takeaway was understanding that middleware promotes code reusability by allowing common functionality to be written once and reused across multiple routes instead of duplicating code throughout the application.

## What changed in my thinking?

Before today, I thought Express simply executed the matching route whenever a request arrived.

After today's learning, I realized that every request passes through multiple layers before reaching the controller. Middleware performs important tasks such as validation, authentication, logging, and error handling before the application's business logic executes.

The biggest realization for me today was that backend development is not only about responding to requests—it is also about designing a structured request-processing pipeline that keeps applications modular, secure, reusable, and scalable.

## Today's One Line Summary

> **"Today I learned how Express routing directs client requests to the correct controllers, while middleware processes requests along the way to build modular, secure, and scalable backend applications."**