# Day 23 - Learning Express.js & Building My First REST APIs

## What did I learn?

Today felt like the day I finally understood what happens behind the scenes when we use a website or an application.

I started learning **Express.js**, and very quickly I realized why almost every Node.js backend uses it. Compared to the built-in HTTP module, Express made everything feel much cleaner and easier to understand. Creating a server, defining routes, and handling requests suddenly didn't seem as complicated as I had imagined.

One of the most interesting parts of today was learning about **REST APIs**. Until now, I knew that the frontend somehow "talked" to the backend, but I never really understood how that communication actually happened. Today, it finally made sense. I learned how requests are sent, how the server processes them, and how responses are returned back to the client.

I also spent time understanding the different HTTP methods like **GET, POST, PUT, PATCH, and DELETE**. Earlier, they were just names I had seen in tutorials, but today I understood why each one exists and when it should be used.

Another concept that stood out was **middleware**. It definitely took me a while to wrap my head around it, but once I understood that middleware acts like a checkpoint where every request can be processed before reaching its destination, everything started clicking into place.

To end the day, I tested my APIs using Postman. Seeing my own server respond with JSON and the correct status codes was surprisingly satisfying. It felt like I wasn't just following tutorials anymore—I was actually beginning to understand how backend applications work.

## What challenges did I face?

The hardest part today was understanding how everything connects together.

At first, I kept wondering what happens after a request reaches the server and where middleware fits into the whole process. It was easy to get lost between routes, middleware, request objects, and responses.

I also mixed up **route parameters, query parameters, and request bodies** a few times because they all seemed to carry data in different ways. After trying a few examples and testing them myself, the differences became much clearer.

There were moments when I had to read the same concept more than once, but every time I practiced it, it started making a little more sense.

## What new concepts did I understand?

### Express Makes Backend Development Simpler

I learned that Express removes a lot of the boilerplate code needed in Node.js and provides a much cleaner way to build backend applications.

### REST APIs

Today I finally understood how the frontend and backend communicate with each other through APIs, and why different HTTP methods exist for different operations.

### Middleware

I learned that middleware sits between the request and the response, allowing the server to perform tasks like validating data, logging requests, handling CORS, or parsing JSON before the request reaches the route.

### Request & Response

I understood how the server receives information through the request object and sends data back using the response object, making the entire communication process much easier to visualize.

## What computer/software engineering fundamentals did I learn today?

Today helped me understand that backend development is all about communication.

Every time we click a button, submit a form, or fetch some data from a website, there's a request traveling to a server and a response coming back. Express makes handling this communication much simpler by organizing routes, middleware, and responses in a structured way.

I also learned why writing clean APIs and returning proper HTTP status codes is an important part of building reliable software.

## What changed in my thinking?

Before today, backend development always felt like something complicated that only experienced developers could understand.

After spending the day with Express, it doesn't feel nearly as intimidating. There's still a lot to learn, but I can finally see how all the pieces fit together.

The biggest realization was that every application I use every day is constantly sending requests and receiving responses. Understanding that process made backend development feel much more real and less like a black box.

Today didn't just teach me a new framework, it gave me a clearer picture of how modern web applications actually work.

## Today's One-Line Summary

> **"Today I finally understood how the frontend and backend talk to each other. Building my first APIs with Express made backend development feel a lot less confusing and a lot more exciting."**
