# Error Handling in Node.js

## What is Error Handling?

While writing programs, errors are unavoidable. A file might not exist, a user may enter invalid input, or a server might fail to connect to a database.

Instead of letting the application crash, Node.js provides different ways to detect and handle these errors gracefully.

Proper error handling helps us:

- Prevent application crashes
- Show meaningful error messages
- Improve debugging
- Build reliable applications

## Types of Errors in Node.js

While learning Node.js, I found that errors can occur for different reasons.

The most common types are:

- Syntax Errors
- Runtime Errors
- Logical Errors
- System Errors
- Custom Errors

## Syntax Errors

Syntax errors occur when the JavaScript code does not follow the language rules.

Example:

```javascript
console.log("Hello"
```

Output:

```text
SyntaxError: missing ) after argument list
```

These errors are detected before the program starts executing.

## Runtime Errors

Runtime errors occur while the program is running.

Example:

```javascript
let user;

console.log(user.name);
```

Output:

```text
TypeError: Cannot read properties of undefined
```

The syntax is correct, but the program fails during execution.

## Logical Errors

Logical errors don't stop the program from running.

Instead, the program runs successfully but produces incorrect output.

Example:

```javascript
let total = 10 + 20 * 5;

console.log(total);
```

If we expected `(10 + 20) * 5`, the output would be incorrect because operator precedence is different.

Logical errors are usually the hardest to find.

## System Errors

System errors occur when Node.js interacts with the operating system.

Examples include:

- File not found
- Permission denied
- Network connection failed
- Port already in use

Example:

```javascript
const fs = require("fs");

fs.readFile("unknown.txt", "utf8", (err, data) => {
    if (err) {
        console.log(err);
    }
});
```

Output:

```text
Error: ENOENT: no such file or directory
```

## JavaScript Error Object

Whenever an error occurs, JavaScript creates an Error object.

Example:

```javascript
try {
    throw new Error("Something went wrong");
}
catch(err){
    console.log(err.message);
}
```

Output:

```text
Something went wrong
```

Some useful properties are:

- `name`
- `message`
- `stack`

Example:

```javascript
try{
    throw new Error("Invalid Input");
}
catch(err){
    console.log(err.name);
    console.log(err.message);
}
```

Output:

```text
Error
Invalid Input
```

## try...catch

Node.js uses `try...catch` to handle synchronous errors.

Example:

```javascript
try{
    let num = 10;

    console.log(num.toUpperCase());
}
catch(err){
    console.log("Error occurred");
    console.log(err.message);
}
```

Output:

```text
Error occurred
num.toUpperCase is not a function
```

The application continues running instead of crashing.

## finally Block

The `finally` block executes whether an error occurs or not.

Example:

```javascript
try{
    console.log("Program started");
}
catch(err){
    console.log(err);
}
finally{
    console.log("Program finished");
}
```

Output:

```text
Program started
Program finished
```

It is commonly used for cleanup operations.

## Throwing Custom Errors

We can create our own errors using the `throw` keyword.

Example:

```javascript
let age = 15;

if(age < 18){
    throw new Error("Age must be at least 18");
}
```

Output:

```text
Error: Age must be at least 18
```

Custom errors help validate user input.

## Error-First Callback Pattern

Most asynchronous Node.js functions follow the error-first callback pattern.

The first parameter always represents an error.

Example:

```javascript
const fs = require("fs");

fs.readFile("message.txt", "utf8", (err, data) => {

    if(err){
        console.log(err);
        return;
    }

    console.log(data);
});
```

If the file is read successfully:

- `err` is `null`
- `data` contains the file content

If something goes wrong:

- `err` contains the error
- `data` is undefined

## Handling File Errors

Example:

```javascript
const fs = require("fs");

fs.readFile("notes.txt", "utf8", (err, data)=>{

    if(err){
        console.log("File not found.");
        return;
    }

    console.log(data);
});
```

Instead of crashing, the program displays a meaningful message.

## Creating Custom Error Classes

Node.js also allows us to create our own error classes.

Example:

```javascript
class ValidationError extends Error{

    constructor(message){
        super(message);
        this.name = "ValidationError";
    }

}

throw new ValidationError("Username is required");
```

Output:

```text
ValidationError: Username is required
```

Custom error classes make applications easier to manage.

## Common JavaScript Errors

Some errors I came across are:

- ReferenceError
- TypeError
- RangeError
- SyntaxError
- URIError
- EvalError

Example:

```javascript
console.log(value);
```

Output:

```text
ReferenceError: value is not defined
```

## Best Practices for Error Handling

Some good practices while writing Node.js applications are:

- Always handle possible errors.
- Use meaningful error messages.
- Never ignore callback errors.
- Use `try...catch` for synchronous code.
- Validate user input before processing.
- Create custom errors when required.
- Avoid exposing sensitive information in error messages.

## Quick Revision

- Errors are a normal part of application development.
- Node.js supports syntax, runtime, logical, and system errors.
- `try...catch` handles synchronous errors.
- `finally` always executes.
- `throw` is used to create custom errors.
- Most asynchronous Node.js APIs follow the error-first callback pattern.
- The Error object contains properties like `name`, `message`, and `stack`.
- Custom error classes improve code organization.
- Proper error handling makes applications reliable and easier to debug.