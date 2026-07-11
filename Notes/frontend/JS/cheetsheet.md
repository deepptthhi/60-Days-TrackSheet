

# 1. Introduction

JavaScript is the programming language of the web. HTML provides
structure, CSS provides styling, and JavaScript adds behavior and
interactivity.

## Features

-   Lightweight
-   Interpreted/JIT compiled
-   Object-oriented
-   Event-driven
-   Cross-platform

# 2. Adding JavaScript

## Inline

``` html
<button onclick="alert('Hello')">Click</button>
```

## Internal

``` html
<script>
console.log("Hello");
</script>
```

## External (Recommended)

``` html
<script src="script.js"></script>
```

# 3. Variables

``` js
let age = 21;
const pi = 3.14;
var oldWay = true;
```

-   `const` → cannot be reassigned.
-   `let` → block scoped.
-   Avoid `var`.

# 4. Data Types

Primitive: - String - Number - Boolean - Undefined - Null - BigInt -
Symbol

Reference: - Object - Array - Function

# 5. Operators

Arithmetic, Assignment, Comparison, Logical, Ternary, Nullish (`??`),
Optional Chaining (`?.`).

# 6. Control Flow

-   if
-   if...else
-   else if
-   switch

# 7. Loops

-   for
-   while
-   do...while
-   for...of
-   for...in

# 8. Functions

-   Normal functions
-   Function expressions
-   Arrow functions
-   Callback functions
-   Higher-order functions
-   Closures

# 9. Arrays

Important methods: - push() - pop() - shift() - unshift() - splice() -
slice() - concat() - map() - filter() - reduce() - find() - some() -
every() - sort()

# 10. Objects

Topics: - Object literals - this keyword - Destructuring - Spread
operator - Rest parameter - Optional chaining

# 11. Strings

Useful methods: - length - slice() - substring() - replace() - trim() -
split() - includes() - startsWith() - endsWith()

# 12. Numbers & Math

Methods: - parseInt() - parseFloat() - toFixed() - Math.random() -
Math.floor() - Math.ceil() - Math.round()

# 13. Dates

``` js
const today = new Date();
```

# 14. Sets & Maps

Set stores unique values.

Map stores key-value pairs with any data type as keys.

# 15. Classes

-   constructor
-   methods
-   inheritance
-   super()

# 16. Asynchronous JavaScript

-   Callbacks
-   Promises
-   async/await
-   Event Loop

# 17. DOM

Selecting Elements: - getElementById() - querySelector() -
querySelectorAll()

Changing: - innerHTML - textContent - style

Events: - click - input - submit - keydown

# 18. Browser APIs

-   Local Storage
-   Session Storage
-   Fetch API
-   Geolocation
-   Timers

# 19. AJAX & Fetch

``` js
fetch(url)
 .then(res=>res.json())
 .then(data=>console.log(data));
```

# 20. JSON

``` js
JSON.stringify(obj);
JSON.parse(text);
```

# 21. Error Handling

``` js
try{

}catch(err){

}finally{

}
```

# 22. Modules

``` js
export
import
```

# 23. Regular Expressions

Used for pattern matching and validation.

# 24. Best Practices

-   Use const whenever possible.
-   Keep functions short.
-   Use meaningful names.
-   Prefer ===.
-   Handle errors.
-   Write reusable code.

# 25. Common Interview Topics

-   Hoisting
-   Scope
-   Closures
-   Event Loop
-   Promises
-   async/await
-   this keyword
-   call/apply/bind
-   Prototype
-   DOM
-   Event Delegation
-   Debouncing
-   Throttling
-   Fetch API
-   Local Storage

# Mini Projects

-   Calculator
-   Digital Clock
-   Stopwatch
-   To-do App
-   Weather App
-   Quiz App
-   Expense Tracker
-   Notes App
-   Portfolio Website

# Quick Cheat Sheet

-   `===` Strict equality
-   `==` Loose equality
-   `let` Block scoped
-   `const` Constant reference
-   `map()` Returns new array
-   `filter()` Filters elements
-   `reduce()` Accumulates values
-   `fetch()` Makes API requests
-   `await` Waits for Promise
-   `querySelector()` Selects first matching element

