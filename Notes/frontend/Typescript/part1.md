# Basics
# TS Home

## What is TypeScript?

TypeScript is a programming language built on top of JavaScript. 
It adds **types**, which help catch mistakes before the code runs.

### Why use it?

-   Finds errors early
-   Makes code easier to understand
-   Great for large projects

# TS Introduction

## Simple Explanation

JavaScript lets you store any type of value in a variable. 
TypeScript lets you define what type of value a variable should hold.

### JavaScript

``` javascript
let age = 20;
age = "Twenty";
```

No error.

### TypeScript

``` typescript
let age: number = 20;
age = "Twenty";
```

Output

    Error: Type 'string' is not assignable to type 'number'.

# TS Get Started

Install:

``` bash
npm install -g typescript
```

Compile:

``` bash
tsc app.ts
```

# TS Simple Types

## Number

``` typescript
let age: number = 22;
```

Output

    22

## String

``` typescript
let name: string = "Deepthi";
```

Output

    Deepthi

## Boolean

``` typescript
let passed: boolean = true;
```

Output

    true

# TS Explicit & Inference

## Explicit

``` typescript
let city: string = "Bangalore";
```

Output

    Bangalore

## Inference

``` typescript
let city = "Bangalore";
```

Output

    Bangalore

TypeScript automatically understands the type.

# TS Special Types

## any

``` typescript
let value:any=10;
value="Hello";
```

Output

    Hello

## unknown

``` typescript
let value:unknown="Hello";
```

Safer than `any`.

## void

``` typescript
function greet():void{
 console.log("Hello");
}
```

Output

    Hello

## never

``` typescript
function error():never{
 throw new Error("Error");
}
```

Output

    Error

# TS Arrays

Arrays store multiple values of the same type.

``` typescript
let fruits:string[]=["Apple","Mango","Banana"];
```

Output

    ["Apple","Mango","Banana"]

# TS Tuples

Tuples store fixed values in a fixed order.

``` typescript
let student:[string,number]=["Deepthi",22];
```

Output

    ["Deepthi",22]

# Quick Revision

-   TypeScript is JavaScript with types.
-   Arrays store same type values.
-   Tuples store fixed values.
-   any is flexible.
-   unknown is safer.
-   void means no return.
-   never means function never finishes normally.
