# Day 35 - Learning REST APIs & CRUD Operations

## What did I learn?

Today, I learned one of the most important concepts in backend development **REST APIs and CRUD operations**. Until now, I understood how Express handled routes and middleware, but I wasn't completely sure how frontend applications actually communicated with the backend. Today's learning helped me understand that APIs act as the bridge between clients and servers, allowing different applications to exchange data over HTTP.

Yesterday, I learned about routing and middleware in Express. That helped me understand how requests travel through an Express application before reaching the controller. Today, I built on that knowledge by learning how backend applications expose RESTful endpoints that clients can use to create, retrieve, update, and delete data.

The first concept I understood today was **Application Programming Interfaces (APIs)**. I learned that an API acts as an interface between two software applications, allowing them to communicate without exposing the internal implementation of the backend. Instead of directly interacting with the database, frontend applications send requests to APIs, and the backend processes those requests before returning the required data.

I then learned about **REST (Representational State Transfer)**. Earlier, I had heard the term "REST API" many times but never fully understood what it meant. Today I learned that REST is a set of architectural principles for designing web APIs. REST APIs use HTTP methods, identify resources through URLs, remain stateless, and typically exchange information using JSON.

Another important concept I learned was **resources**. Instead of creating URLs based on actions, REST APIs identify objects such as users, products, and orders using resource-based URLs. For example, `/users` represents the user resource, while `/products` represents product-related operations. This makes APIs more consistent and easier to understand.

I also explored the different **HTTP methods** used while building REST APIs. Although I had previously learned what GET, POST, PUT, PATCH, and DELETE meant, today I understood how they directly correspond to CRUD operations. GET retrieves data, POST creates new resources, PUT replaces existing resources, PATCH updates specific fields, and DELETE removes resources. This helped me understand how backend applications expose standardized operations for managing data.

One of the biggest topics I learned today was **CRUD operations**. CRUD stands for Create, Read, Update, and Delete, which represent the four fundamental operations performed on almost every database. I realized that nearly every real-world application, whether it is an e-commerce platform, banking system, or social media application, performs these operations through REST APIs.

Another concept I understood today was **HTTP status codes**. Earlier, I had seen status codes such as 200 and 404 without paying much attention to them. Today I learned that status codes allow the server to communicate the outcome of a request to the client. Successful requests return codes like 200 OK or 201 Created, while unsuccessful requests return codes such as 400 Bad Request, 404 Not Found, or 500 Internal Server Error.

I also learned about **JSON (JavaScript Object Notation)**. Although I had worked with JSON before, today I understood why it is the most commonly used data format in REST APIs. JSON is lightweight, human-readable, and supported by almost every programming language, making it ideal for exchanging data between clients and servers.

Towards the end of today's learning, I explored how developers **test APIs using Postman**. Before today, I assumed that a frontend application was always required to test backend functionality. I learned that Postman allows developers to send HTTP requests directly to the backend, inspect responses, verify status codes, and debug APIs without building a user interface.

Finally, I learned several **REST API best practices**. I understood the importance of using meaningful resource names, returning appropriate HTTP status codes, validating incoming request data, and consistently returning JSON responses. These practices help developers create APIs that are reliable, maintainable, and easy for other developers to use.

By the end of today's learning, I realized that REST APIs are the foundation of modern web development. They enable frontend applications, mobile applications, and third-party services to communicate with backend systems in a standardized, scalable, and platform independent manner.

## What challenges did I face?

The biggest challenge today was understanding the difference between an **API** and **REST**. Initially, I thought both terms referred to the same thing. After studying the concepts, I realized that an API is a communication interface, while REST is a set of architectural principles used to design APIs.

Another challenge was understanding the difference between **PUT** and **PATCH** requests. At first, both appeared to perform updates. After learning more, I understood that PUT replaces an entire resource, whereas PATCH updates only specific fields without replacing the complete resource.

I also found it slightly confusing to understand how HTTP methods relate to CRUD operations. Once I mapped each HTTP method to its corresponding database operation, the relationship became much clearer.

## What new concepts did I understand?

### API

I learned that an API acts as an interface that enables communication between different software applications.

### REST

I understood that REST is an architectural style used to design scalable and standardized web APIs.

### Resources

I learned that REST APIs organize endpoints around resources such as users, products, and orders instead of actions.

### CRUD Operations

I understood that Create, Read, Update, and Delete are the four fundamental database operations performed through REST APIs.

### HTTP Methods

I learned how GET, POST, PUT, PATCH, and DELETE methods correspond to CRUD operations while designing RESTful APIs.

### HTTP Status Codes

I understood that status codes communicate whether a request succeeded or failed and provide meaningful information to the client.

### JSON

I learned that JSON is the standard format used to exchange structured data between clients and servers.

### Postman

I understood how Postman allows developers to test APIs by sending HTTP requests and inspecting responses without requiring a frontend application.

### REST API Best Practices

I learned the importance of using resource based URLs, meaningful status codes, JSON responses, and proper request validation when designing production-ready APIs.

## What computer/software engineering fundamentals did I learn today?

Today's learning helped me understand one of the most important principles in software engineering **standardized communication between software systems**. REST APIs provide a common interface that allows different applications to exchange information regardless of the technologies used to build them.

I also realized that backend applications should expose clear, predictable, and consistent endpoints that follow REST conventions. Using standardized HTTP methods and status codes improves maintainability, scalability, and collaboration between frontend and backend developers.

Another important takeaway was understanding that APIs should remain stateless. Every request should contain all the information needed for processing, allowing applications to scale efficiently across multiple servers.

## What changed in my thinking?

Before today, I thought backend applications simply responded to requests from the frontend without following any particular standard.

After today's learning, I realized that professional backend systems are designed around REST principles, standardized HTTP methods, meaningful URLs, and structured JSON responses. These standards allow different applications and services to communicate reliably and consistently.

The biggest realization for me today was that building a backend is not only about writing server-side code—it is about designing APIs that other developers and applications can easily understand, integrate with, and maintain.

## Today's One Line Summary

> **"Today I learned how REST APIs use standardized HTTP methods and CRUD operations to enable secure, scalable, and structured communication between clients and backend applications."**