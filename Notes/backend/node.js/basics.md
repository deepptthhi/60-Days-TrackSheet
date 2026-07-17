

## What is Node.js?

When I started learning Node.js, the first thing I wanted to know was whether it was a programming language. It turns out that it isn't.

Node.js is an **open-source, cross-platform JavaScript runtime environment** that allows us to run JavaScript outside the browser. Earlier, JavaScript was mainly used for frontend development, but Node.js made it possible to build backend applications using the same language.

Node.js is built on **Google Chrome's V8 JavaScript Engine**, which converts JavaScript code into machine code and executes it very efficiently.

## Why Node.js?

Before Node.js, developers usually had to learn different languages for frontend and backend development.

For example:

- Frontend → HTML, CSS, JavaScript
- Backend → Java, PHP, Python, C#, etc.

With Node.js, JavaScript can be used for both frontend and backend, making full-stack development much easier.

Node.js is commonly used to build:

- REST APIs
- Backend servers
- Chat applications
- Real-time applications
- Streaming platforms
- Command-line tools
- Microservices

## Features of Node.js

### Fast Execution

Node.js is built on Google's V8 Engine, which compiles JavaScript into machine code very quickly. This makes Node.js applications fast and efficient.

### Asynchronous

Node.js performs tasks asynchronously.

Instead of waiting for one task to finish before starting another, it continues executing other operations while the first one runs in the background.

This improves the overall performance of an application.

### Event Driven

Node.js follows an event-driven architecture.

Whenever an event occurs, such as a user sending a request or uploading a file, Node.js responds to that event.

Examples of events include:

- User requests
- File uploads
- Database responses
- Timer completion

### Non-Blocking I/O

Node.js does not block the execution of other tasks while waiting for an operation like reading a file or fetching data from a database.

Instead, it keeps handling other requests, making applications highly responsive.

### Single Threaded

Although Node.js runs on a single thread, it can still manage thousands of client requests efficiently.

It achieves this using the Event Loop and asynchronous programming instead of creating multiple threads for every request.

### Cross Platform

Node.js applications can run on different operating systems such as:

- Windows
- Linux
- macOS

without changing the source code.

## Node.js Architecture

One of the most interesting things I learned is how Node.js handles multiple users even though it uses only one thread.

The architecture mainly consists of:

- Client Requests
- Event Queue
- Event Loop
- Thread Pool
- Operating System

Whenever a request takes time, like reading a file, Node.js sends that task to the system instead of waiting.

Meanwhile, the Event Loop continues processing new incoming requests.

Once the background task finishes, its result is returned to the Event Loop and then sent back to the client.

This architecture is one of the biggest reasons why Node.js performs so well.

## Installing Node.js

Download Node.js from the official website and install it.

After installation, verify it using:

```bash
node -v
```

Check npm version:

```bash
npm -v
```

If both commands return version numbers, Node.js has been installed successfully.

## Creating a Node.js Project

Create a new folder.

```bash
mkdir node-project
```

Move inside the folder.

```bash
cd node-project
```

Initialize the project.

```bash
npm init -y
```

This creates a **package.json** file that stores project information and dependencies.

## Writing the First Node.js Program

Create a file named:

```text
app.js
```

Write the following code:

```javascript
console.log("Hello Node.js");
```

Run it using:

```bash
node app.js
```

Output:

```text
Hello Node.js
```

Unlike browser JavaScript, this program runs directly from the terminal.

## Creating Your First Server

Node.js provides a built-in **http** module that helps us create web servers.

Example:

```javascript
const http = require("http");

const server = http.createServer((req, res) => {
    res.write("Hello World!");
    res.end();
});

server.listen(3000, () => {
    console.log("Server running on port 3000");
});
```

Run the server:

```bash
node app.js
```

Visit:

```
http://localhost:3000
```

The browser will display:

```
Hello World!
```

This is the simplest example of creating a backend server using Node.js.

## Understanding Request and Response

Whenever a browser accesses a website, it sends a **request** to the server.

The server processes the request and sends back a **response**.

Every Node.js server follows this request-response cycle.

## Modules in Node.js

Node.js organizes code using modules.

A module is simply a reusable piece of code that can be imported into another file.

There are mainly three types of modules:

- Core Modules
- Local Modules
- Third-Party Modules

Some commonly used core modules are:

### HTTP Module

Used for creating web servers.

### File System (FS)

Used for reading, writing, updating, deleting, and managing files.

### Path Module

Helps in working with file and folder paths.

### Events Module

Used to create and handle custom events.

These modules are built into Node.js, so no installation is required.

## Event Loop

The Event Loop was one of the most interesting concepts I came across.

Initially, I wondered how a single-threaded application could handle thousands of users.

The answer is the Event Loop.

Whenever an operation takes time, such as reading a file or querying a database, Node.js doesn't stop the entire program.

Instead, it continues handling new requests.

Once the long-running task is complete, the Event Loop brings the result back and finishes the execution.

This allows Node.js to remain fast even when many users access the application simultaneously.

## Advantages of Node.js

Some advantages I learned are:

- High performance
- Fast execution
- Scalable
- Cross-platform support
- Large npm ecosystem
- JavaScript for both frontend and backend
- Suitable for real-time applications

## Limitations of Node.js

Although Node.js is very powerful, it isn't the best choice for CPU-intensive tasks.

Applications involving heavy image processing, video rendering, or complex mathematical computations can block the Event Loop and reduce performance.

## Quick Revision

- Node.js is a JavaScript runtime environment.
- It is built on Google's V8 Engine.
- It allows JavaScript to run outside the browser.
- Node.js follows an event-driven and non-blocking architecture.
- It uses asynchronous programming to improve performance.
- The Event Loop helps Node.js handle multiple requests efficiently.
- Built-in modules like HTTP, FS, Path, and Events make backend development easier.
- Node.js is commonly used for APIs, backend servers, and real-time applications.