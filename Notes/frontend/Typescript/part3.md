# Classes & Advanced Basics

# TS Classes

## Simple Explanation

A class is like a blueprint for creating objects. 
It helps us group data and functions together.

### Syntax

``` typescript
class Student {
  name: string;
  age: number;

  constructor(name: string, age: number) {
    this.name = name;
    this.age = age;
  }

  display() {
    console.log(this.name, this.age);
  }
}

const s1 = new Student("Deepthi", 22);
s1.display();
```

Output

    Deepthi 22

## Access Modifiers

### public

Anyone can access it.

``` typescript
class Student {
  public name = "Deepthi";
}
```

### private

Can only be used inside the class.

``` typescript
class Student {
  private password = "1234";
}
```

### protected

Can be used inside the class and child classes.

``` typescript
class Person {
  protected age = 22;
}
```

# TS Basic Generics

## Simple Explanation

Generics let us write reusable code that works with different data types.

### Without Generic

``` typescript
function show(value: string) {
  return value;
}
```

Works only for strings.

### With Generic

``` typescript
function show<T>(value: T): T {
  return value;
}

console.log(show("Hello"));
console.log(show(100));
```

Output

    Hello
    100

# TS Utility Types

## Simple Explanation

Utility types are built-in helpers that make working with types easier.

## Partial

Makes all properties optional.

``` typescript
interface Student {
  name: string;
  age: number;
}

const s: Partial<Student> = {
  name: "Deepthi"
};
```

Output

    { name: "Deepthi" }

## Required

Makes every property mandatory.

``` typescript
interface User {
  name?: string;
}

const u: Required<User> = {
  name: "Rahul"
};
```

Output

    { name: "Rahul" }

## Readonly

Prevents values from being changed.

``` typescript
interface Book {
  title: string;
}

const b: Readonly<Book> = {
  title: "React"
};
```

Trying to change `title` gives an error.

# TS Keyof

## Simple Explanation

`keyof` gives all the property names of an object as a type.

### Syntax

``` typescript
interface Student {
  name: string;
  age: number;
}

type Keys = keyof Student;
```

Output

    "name" | "age"

Example

``` typescript
let key: Keys = "name";
```

Output

    name

# TS Null

## Simple Explanation

`null` means a variable intentionally has no value.

### Syntax

``` typescript
let value: string | null = null;

value = "Hello";

console.log(value);
```

Output

    Hello

Using union types allows a variable to store either a string or null.

# TS Definitely Typed

## Simple Explanation

Many JavaScript libraries don't include TypeScript support by default.

Definitely Typed provides type definitions for those libraries.

### Install

``` bash
npm install --save-dev @types/lodash
```

Example

``` typescript
import _ from "lodash";
```

Now TypeScript understands lodash functions and provides autocomplete.

# Quick Revision

-   Classes are blueprints for creating objects.
-   Constructors initialize object values.
-   public is accessible everywhere.
-   private is accessible only inside the class.
-   protected is accessible inside the class and subclasses.
-   Generics make functions reusable for different types.
-   Utility types simplify working with existing types.
-   keyof returns property names of an object.
-   null represents no value.
-   Definitely Typed adds TypeScript support to JavaScript libraries.
