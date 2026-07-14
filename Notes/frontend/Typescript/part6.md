# Advanced Concepts



# TS Namespaces

## Simple Explanation

Namespaces help organize related code into one group and avoid naming conflicts.

### Syntax

``` typescript
namespace StudentData {
  export const name = "Deepthi";

  export function greet() {
    console.log("Hello " + name);
  }
}

StudentData.greet();
```

Output

    Hello Deepthi

Namespaces are mostly used in older TypeScript projects. Modern projects usually use ES Modules instead.

# TS Index Signatures

## Simple Explanation

Index signatures allow an object to have dynamic property names while keeping the value type fixed.

### Syntax

``` typescript
interface Marks {
  [subject: string]: number;
}

const student: Marks = {
  Math: 95,
  Science: 90,
  English: 88
};

console.log(student);
```

Output

    { Math: 95, Science: 90, English: 88 }

# TS Declaration Merging

## Simple Explanation

Declaration merging allows multiple declarations with the same name to combine into one.

### Example

``` typescript
interface Student {
  name: string;
}

interface Student {
  age: number;
}

const s: Student = {
  name: "Deepthi",
  age: 22
};

console.log(s);
```

Output

    { name: "Deepthi", age: 22 }

This feature is mostly used while extending existing libraries.

# TS Async Programming

## Simple Explanation

Async programming helps run tasks like API calls without blocking the application.

### Async Function

``` typescript
async function greet() {
  return "Hello";
}

greet().then(console.log);
```

Output

    Hello

### Await Example

``` typescript
async function fetchData() {
  const data = await Promise.resolve("Data Loaded");
  console.log(data);
}

fetchData();
```

Output

    Data Loaded

`async` makes a function return a Promise, and `await` waits until the Promise is completed.

# TS Decorators

## Simple Explanation

Decorators are special functions that add extra behavior to classes, methods, or properties without changing their original code.

They are commonly used in frameworks like Angular and NestJS.

### Example

``` typescript
function Logger(constructor: Function) {
  console.log("Class Created");
}

@Logger
class Student {}
```

Output

    Class Created

To use decorators, they must be enabled in `tsconfig.json`.

``` json
{
  "experimentalDecorators": true
}
```

# When are these used?

-   Namespaces → Older TypeScript projects
-   Index Signatures → Dynamic object properties
-   Declaration Merging → Extending interfaces
-   Async Programming → API calls and database operations
-   Decorators → Angular, NestJS, metadata-based programming

# Quick Revision

-   Namespaces organize related code.
-   Index signatures allow dynamic keys.
-   Declaration merging combines declarations with the same name.
-   Async and await handle asynchronous operations.
-   Decorators add functionality without modifying the original code.
