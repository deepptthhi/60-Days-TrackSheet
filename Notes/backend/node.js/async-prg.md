# Asynchronous Programming in Node.js

## What is Asynchronous Programming?

Asynchronous Programming allows Node.js to execute long-running tasks in the background instead of waiting for them to finish. This makes applications faster and more responsive.

Examples of asynchronous tasks include: - Reading files - Making API requests - Database operations - Network communication

## Why Do We Need Asynchronous Programming?

Imagine ordering food at a restaurant. After placing your order, you don't stand in the kitchen waiting for it to be prepared. Instead, you sit at your table while the chef cooks your meal. Similarly, Node.js continues handling other tasks while waiting for time-consuming operations to finish.

Benefits: - Better performance - High scalability - Improved user experience - Efficient resource utilization

## Synchronous vs Asynchronous Programming

### Synchronous Programming

Each statement waits for the previous one to finish.

``` javascript
console.log("Start");
console.log("Processing...");
console.log("End");
```

Output:

``` text
Start
Processing...
End
```

### Asynchronous Programming

Long-running tasks execute in the background.

``` javascript
console.log("Start");

setTimeout(() => {
    console.log("Task Completed");
}, 2000);

console.log("End");
```

Output:

``` text
Start
End
Task Completed
```

## Blocking vs Non-Blocking I/O

### Blocking I/O

The program waits until the operation finishes.

``` javascript
const fs = require("fs");

const data = fs.readFileSync("message.txt", "utf8");
console.log(data);
console.log("Finished");
```

### Non-Blocking I/O

The program continues executing while the operation runs in the
background.

``` javascript
const fs = require("fs");

fs.readFile("message.txt", "utf8", (err, data) => {
    if (err) {
        console.log(err);
        return;
    }

    console.log(data);
});

console.log("Finished");
```

## How Node.js Handles Asynchronous Tasks

``` text
Client Request
      │
      ▼
 Node.js Runtime
      │
      ▼
 Event Loop
      │
      ▼
Operating System / Thread Pool
      │
      ▼
Callback Queue
      │
      ▼
Response Returned
```

## Event Loop

The Event Loop is the heart of Node.js. It continuously checks whether background tasks have completed. Once a task is finished, its callback is moved to the Call Stack for execution.

Responsibilities: - Handles asynchronous tasks - Executes callbacks - Keeps the application responsive - Allows Node.js to manage many requests simultaneously

## Callbacks

A callback is a function passed as an argument to another function and executed after a task completes.

``` javascript
function greet(name, callback) {
    console.log("Hello " + name);
    callback();
}

function goodbye() {
    console.log("Goodbye!");
}

greet("Deepthi", goodbye);
```

Output:

``` text
Hello Deepthi
Goodbye!
```

## Callback Hell

Deeply nested callbacks reduce readability.

``` javascript
login(function () {
    getProfile(function () {
        getOrders(function () {
            makePayment(function () {
                console.log("Done");
            });
        });
    });
});
```

This is known as Callback Hell.

## Promises

Promises simplify asynchronous programming and avoid callback hell.

Promise States: - Pending - Fulfilled - Rejected

``` javascript
const promise = new Promise((resolve, reject) => {
    let success = true;

    if (success) {
        resolve("Task Completed");
    } else {
        reject("Task Failed");
    }
});

promise
.then(result => console.log(result))
.catch(error => console.log(error));
```

## Promise Chaining

``` javascript
Promise.resolve(5)
.then(num => num * 2)
.then(num => num + 10)
.then(result => console.log(result));
```

Output:

``` text
20
```

## Async and Await

`async` and `await` make asynchronous code easier to read.

``` javascript
function fetchData() {
    return new Promise(resolve => {
        setTimeout(() => {
            resolve("Data Loaded");
        }, 2000);
    });
}

async function display() {
    const result = await fetchData();
    console.log(result);
}

display();
```

## EventEmitter

Node.js uses events internally. The EventEmitter class lets us create and trigger custom events.

``` javascript
const EventEmitter = require("events");

const event = new EventEmitter();

event.on("login", () => {
    console.log("User Logged In");
});

event.emit("login");
```

## Timers

### setTimeout()

``` javascript
setTimeout(() => {
    console.log("Runs after 2 seconds");
}, 2000);
```

### setInterval()

``` javascript
setInterval(() => {
    console.log("Running...");
}, 1000);
```

### clearInterval()

``` javascript
const timer = setInterval(() => {
    console.log("Running...");
}, 1000);

clearInterval(timer);
```

## Best Practices

-   Prefer asynchronous APIs over synchronous ones.
-   Use Promises instead of deeply nested callbacks.
-   Use async/await for cleaner code.
-   Always handle Promise rejections.
-   Avoid blocking the Event Loop.
-   Keep callbacks small and reusable.

## Quick Revision

-   Node.js is asynchronous by default.
-   Asynchronous programming improves performance.
-   Blocking code waits for completion.
-   Non-blocking code continues executing.
-   Callbacks execute after a task finishes.
-   Callback Hell reduces code readability.
-   Promises simplify asynchronous code.
-   Async/await improves readability.
-   The Event Loop manages asynchronous execution.
-   EventEmitter enables custom events.
-   Timers help schedule tasks.
