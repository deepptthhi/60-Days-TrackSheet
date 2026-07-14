# Real-World TypeScript


# TS in JavaScript Projects

## Simple Explanation

You don't have to rewrite an entire JavaScript project to use TypeScript. 
You can slowly add TypeScript files whenever you're ready.

For example:

    project/
    │
    ├── app.js
    ├── user.js
    ├── product.ts
    └── index.ts

This makes migration easier for large projects.

# TS Migration

## Simple Explanation

Migrating means converting a JavaScript project into a TypeScript
project one file at a time.

### Steps

1.  Install TypeScript

``` bash
npm install typescript --save-dev
```

2.  Create a configuration file

``` bash
tsc --init
```

3.  Rename files

```{=html}
<!-- -->
```
    app.js
    ↓

    app.ts

4.  Fix type errors one by one.

Migration takes time, but it makes the project safer and easier to
maintain.

# TS Error Handling

## Simple Explanation

TypeScript doesn't replace JavaScript error handling. It simply helps catch many mistakes before your code runs.

### Example

``` typescript
try {
  let data = JSON.parse('{"name":"Deepthi"}');
  console.log(data.name);
} catch (error) {
  console.log("Something went wrong.");
}
```

Output

    Deepthi

If parsing fails:

    Something went wrong.

# TS Best Practices

## Use Interfaces for Objects

``` typescript
interface Student {
  name: string;
  age: number;
}
```

## Avoid using any

❌

``` typescript
let value: any;
```

✅

``` typescript
let value: string;
```

## Enable Strict Mode

Inside **tsconfig.json**

``` json
{
  "strict": true
}
```

This helps catch more errors.

## Use Meaningful Names

❌

``` typescript
let a = "Deepthi";
```

✅

``` typescript
let studentName = "Deepthi";
```

Meaningful names make code easier to understand.

# Common Interview Questions

## What is TypeScript?

TypeScript is JavaScript with static typing. It helps detect errors during development instead of at runtime.

## Why use TypeScript?

-   Better code quality
-   Better autocomplete
-   Easier debugging
-   Easier maintenance

## Difference between any and unknown?

-   `any` allows any operation.
-   `unknown` requires checking the type before using it.

## Difference between Interface and Type?

-   Interface is mainly used for objects.
-   Type is more flexible and can represent many kinds of types.

## Difference between null and undefined?

-   `null` means intentionally empty.
-   `undefined` means a value hasn't been assigned.

## What are Generics?

Generics make functions, classes, and interfaces reusable for different data types.

# Common Beginner Mistakes

-   Using `any` everywhere.
-   Forgetting to enable strict mode.
-   Not understanding interfaces.
-   Ignoring compiler errors.
-   Using type assertions without checking values.

# Cheat Sheet

  Feature       Purpose
  ------------- ---------------------------
  Interface     Object structure
  Type Alias    Reusable custom type
  Enum          Fixed set of values
  Union         Multiple possible types
  Generic       Reusable code
  keyof         Get object keys
  Partial       Make properties optional
  Readonly      Prevent changes
  Type Guard    Check type safely
  Async/Await   Handle asynchronous tasks

# Real-World Folder Structure

    src/
    │
    ├── components/
    ├── pages/
    ├── services/
    ├── hooks/
    ├── utils/
    ├── types/
    ├── interfaces/
    ├── App.tsx
    └── main.tsx

Keeping types and interfaces in separate folders makes large projects easier to manage.

# Quick Revision

-   TypeScript can be added gradually to JavaScript projects.
-   Migration happens one file at a time.
-   Use try...catch for runtime errors.
-   Avoid using `any`.
-   Prefer interfaces for object structures.
-   Enable strict mode.
-   Learn compiler errors instead of ignoring them.
-   Write clean and meaningful code.

# Final Note

Learning TypeScript is not about memorizing every feature. The most
important goal is understanding how types help you write safer, cleaner,and more maintainable code. As you build React or Node.js projects,you'll naturally become more comfortable with TypeScript and start appreciating how much time it saves by catching mistakes early.
