# Day 30 - Learning REST APIs with Express.js

## What did I learn?

Today I learned one of the most important topics in backend development **REST APIs**. Before today, I knew how to create routes in Express, but I didn't really understand how a frontend application communicates with the backend. After today's learning, everything started connecting together, and I could finally see the complete picture of how a request travels from the client to the server and back.

The first thing I understood was what an **API (Application Programming Interface)** actually is. Earlier, I always heard people say, "Create an API" or "Call an API," but I never thought deeply about what it really meant. Today I realized that an API is simply a bridge that allows two applications to communicate. Whenever we use an app like Instagram or Amazon, the frontend doesn't directly access the database. Instead, it sends a request to the backend through an API, the backend processes the request, fetches the required data, and sends the response back.

I also learned about **REST (Representational State Transfer)** and why almost every modern application follows REST principles. I understood that REST is not a technology but a set of rules for designing APIs in a clean and organized way. Instead of creating random URLs, APIs are designed around resources like users, products, or orders, making them easier for developers to understand and maintain.

One of the biggest things I learned today was the purpose of different **HTTP methods**. Until now, I knew the names GET and POST, but I wasn't very confident about when each one should be used. Today I learned that GET is used to retrieve data, POST is used to create new data, PUT replaces an existing resource, PATCH updates only selected fields, and DELETE removes data. Once I connected these methods with CRUD operations, they became much easier to remember.

Another concept that finally became clear was **API endpoints**. Earlier, every route looked almost the same to me, but now I understand that each endpoint represents a specific resource or action. For example, `/users` returns all users, while `/users/:id` returns details of a single user. This made me realize that designing APIs is more about organizing resources than simply writing routes.

I also spent time understanding the difference between **Route Parameters** and **Query Parameters**. At first, I found them confusing because both appear in the URL. After practicing a few examples, I realized that route parameters identify a specific resource, while query parameters are mainly used for filtering, searching, sorting, or pagination. That small difference cleared up a confusion I had for quite some time.

Another important thing I learned was how the frontend sends data to the backend using the **request body**. I understood that when creating or updating data, the client sends information in JSON format, and Express converts that JSON into a JavaScript object using `express.json()`. Before today, I had used this middleware without really knowing why it was needed. Now I understand its purpose much better.

I also learned how the backend sends responses back to the client. Instead of simply returning text, most applications return **JSON** because it is lightweight, easy to read, and supported by almost every programming language. Understanding why JSON has become the standard format for communication made the entire request-response cycle much clearer.

Towards the end, I learned about **HTTP status codes**. Earlier, I only knew that 404 meant "Page Not Found." Today I learned that status codes are much more meaningful than I thought. Codes like 200, 201, 400, 401, 403, 404, and 500 help the client understand whether the request was successful or if something went wrong. I realized that returning the correct status code is an important part of writing professional APIs.

Finally, I built a simple REST API using Express.js and tested it using **Postman** and **Thunder Client**. Sending requests manually and seeing the responses helped me understand the complete lifecycle of an API much better than just reading theory. Watching the request go from the client, through the server, and back as a response made everything feel much more practical.

By the end of today's learning, I realized that almost every modern application depends on REST APIs. Whether it's a website, a mobile application, or even communication between two backend services, APIs are the backbone that allows everything to work together.

## What challenges did I face?

The biggest challenge today was understanding how all the concepts fit together. I already knew about routes, JSON, and HTTP methods separately, but I couldn't clearly picture the complete flow of a request. Once I followed the journey from the client sending a request to the server processing it and returning a response, everything started making much more sense.

I also found it slightly confusing to differentiate between **Route Parameters** and **Query Parameters** because both are part of the URL. After trying multiple examples, I finally understood when each one should be used.

Another small challenge was remembering which HTTP method matches which CRUD operation. Initially, I had to think twice before choosing between PUT and PATCH, but after enough examples, the differences became much clearer.

## What new concepts did I understand?

### API

I learned that an API acts as a bridge that allows different applications to communicate with each other.

### REST

I understood that REST is a standard way of designing APIs so they remain simple, organized, and easy to maintain.

### HTTP Methods

I learned how GET, POST, PUT, PATCH, and DELETE are used to perform different operations on data.

### CRUD Operations

I understood how Create, Read, Update, and Delete operations directly map to different HTTP methods.

### API Endpoints

I learned that every endpoint represents a specific resource or functionality within an application.

### Route Parameters

I understood that route parameters identify a particular resource using values inside the URL.

### Query Parameters

I learned that query parameters are mainly used for filtering, searching, sorting, and pagination.

### Request Body

I understood how the client sends JSON data to the backend and how Express accesses it through `req.body`.

### HTTP Status Codes

I learned why returning meaningful status codes is important for both developers and frontend applications.

### API Testing

I learned how tools like Postman and Thunder Client help developers test APIs before integrating them with the frontend.

## What computer/software engineering fundamentals did I learn today?

Today's learning helped me understand that APIs are one of the core building blocks of software engineering. Almost every application today depends on APIs to exchange information between different systems.

I also realized that writing a working API isn't enough. Good API design means using meaningful endpoints, choosing the correct HTTP methods, returning proper status codes, and keeping communication between the frontend and backend clean and consistent.

Another important thing I understood is that frontend and backend are designed to work independently. The frontend focuses on the user interface, while the backend handles business logic and data. APIs connect these two layers without tightly coupling them together.

## What changed in my thinking?

Before today, I used to think APIs were just Express routes that returned some data.

After today's learning, I realized that APIs are actually well-designed communication interfaces that define how applications talk to each other. Every request follows a proper structure using HTTP methods, endpoints, request bodies, JSON responses, and status codes.

The biggest realization for me today was that building good APIs isn't just about making things work, it's about making them predictable, organized, and easy for other developers to use.

## Today's One Line Summary

> **"Today I learned how REST APIs allow the frontend and backend to communicate using HTTP requests, JSON, and proper API design, helping me understand how modern web applications work behind the scenes."**