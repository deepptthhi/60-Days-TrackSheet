# Node.js Core Modules

One thing I noticed while learning Node.js is that it already provides many useful modules, so we don't always have to install external libraries.

These built-in modules help us perform common tasks like working with files, creating servers, handling events, and interacting with the operating system.

Since they are built into Node.js, we can use them directly with the `require()` function.

``` javascript
const fs = require("fs");
```

This imports the File System module.

Some of the most commonly used core modules are:

-   HTTP
-   File System (FS)
-   Path
-   OS
-   Events
-   Buffer


# File System (FS) Module

The File System module allows Node.js to work with files on our computer.

Using this module, we can:

-   Create files
-   Read files
-   Write data into files
-   Update files
-   Delete files
-   Rename files

Import the module:

``` javascript
const fs = require("fs");
```

## Reading a File

Suppose we have a file called `message.txt`.

``` javascript
const fs = require("fs");

fs.readFile("message.txt", "utf8", (err, data) => {
    if (err) {
        console.log(err);
        return;
    }

    console.log(data);
});
```

### Explanation

-   `readFile()` reads the contents of a file.
-   `"utf8"` converts the file into readable text.
-   The callback runs after the file has been read.
-   If an error occurs, it is stored in `err`.
-   Otherwise, the file content is stored in `data`.

## Writing to a File

We can create a new file or overwrite an existing one.

``` javascript
fs.writeFile("message.txt", "Learning Node.js!", (err) => {
    if (err) throw err;

    console.log("File created successfully.");
});
```

If the file doesn't exist, Node.js creates it automatically.

## Appending Data

``` javascript
fs.appendFile("message.txt", "\nNode.js is awesome!", (err) => {
    if (err) throw err;

    console.log("Data added.");
});
```

## Deleting a File

``` javascript
fs.unlink("message.txt", (err) => {
    if (err) throw err;

    console.log("File deleted.");
});
```


# Path Module

The Path module helps us create file paths that work correctly across operating systems.

``` javascript
const path = require("path");
```

## Getting File Name

``` javascript
console.log(path.basename("/users/project/app.js"));
```

Output:

``` text
app.js
```

## Getting File Extension

``` javascript
console.log(path.extname("app.js"));
```

Output:

``` text
.js
```

## Joining Paths

``` javascript
const filePath = path.join("users", "deepthi", "documents");

console.log(filePath);
```


# OS Module

The OS module provides information about the operating system.

``` javascript
const os = require("os");

console.log(os.platform());
console.log(os.arch());
console.log(os.cpus().length);
console.log(os.totalmem());
```

Useful methods:

-   `os.platform()`
-   `os.arch()`
-   `os.hostname()`
-   `os.totalmem()`
-   `os.freemem()`



# Events Module

Node.js is built around events.

``` javascript
const EventEmitter = require("events");

const event = new EventEmitter();

event.on("greet", () => {
    console.log("Welcome to Node.js");
});

event.emit("greet");
```

Output:

``` text
Welcome to Node.js
```

-   `on()` listens for an event.
-   `emit()` triggers the event.



# Buffer Module

Buffers help Node.js handle binary data like images, videos, audio files, and network communication.

``` javascript
const buffer = Buffer.from("Hello");

console.log(buffer);
```

Output:

``` text
<Buffer 48 65 6c 6c 6f>
```


# Global Objects

Node.js provides global objects without importing anything.

``` javascript
console.log(__dirname);
console.log(__filename);
```

-   `__dirname` returns the current folder.
-   `__filename` returns the current file.



# Exporting Modules

**math.js**

``` javascript
function add(a, b) {
    return a + b;
}

module.exports = add;
```

**app.js**

``` javascript
const add = require("./math");

console.log(add(10, 20));
```

Output:

``` text
30
```


# Importing Multiple Functions

``` javascript
function add(a, b) {
    return a + b;
}

function subtract(a, b) {
    return a - b;
}

module.exports = {
    add,
    subtract
};
```

``` javascript
const math = require("./math");

console.log(math.add(5, 2));
console.log(math.subtract(5, 2));
```


# CommonJS

Node.js traditionally uses the CommonJS module system.

Import:

``` javascript
require()
```

Export:

``` javascript
module.exports
```


# Error Handling

Most asynchronous Node.js functions follow the error-first callback pattern.

``` javascript
fs.readFile("test.txt", "utf8", (err, data) => {
    if (err) {
        console.log(err);
        return;
    }

    console.log(data);
});
```


# Quick Revision

-   Node.js provides many built-in modules.
-   The File System module is used to read, write, update, and delete files.
-   The Path module helps create file paths safely.
-   The OS module provides system information.
-   The Events module allows us to create custom events.
-   Buffers are used for binary data.
-   `__dirname` and `__filename` are global objects.
-   `module.exports` exports code and `require()` imports it.
-   Node.js mainly uses the CommonJS module system.
-   Most asynchronous functions follow the error-first callback pattern.
