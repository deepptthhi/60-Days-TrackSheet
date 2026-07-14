# Objects & Functions


# TS Object Types

## Simple Explanation

Objects store related information together using key-value pairs.

### Syntax

``` typescript
let student: { name: string; age: number } = {
  name: "Deepthi",
  age: 22
};
```

Output

    { name: "Deepthi", age: 22 }

# TS Enums

## Simple Explanation

Enums let us give meaningful names to a group of related values.

### Syntax

``` typescript
enum Direction {
  Up,
  Down,
  Left,
  Right
}

let move: Direction = Direction.Up;
console.log(move);
```

Output

    0

String Enum

``` typescript
enum Status {
  Success = "SUCCESS",
  Failed = "FAILED"
}

console.log(Status.Success);
```

Output

    SUCCESS

# TS Type Aliases

## Simple Explanation

A type alias lets you give a custom name to a type so you can reuse it.

### Syntax

``` typescript
type Student = {
  name: string;
  age: number;
};

let s: Student = {
  name: "Deepthi",
  age: 22
};
```

Output

    { name: "Deepthi", age: 22 }

# TS Interfaces

## Simple Explanation

Interfaces define the structure that an object should follow.

### Syntax

``` typescript
interface Employee {
  name: string;
  salary: number;
}

let emp: Employee = {
  name: "Rahul",
  salary: 50000
};
```

Output

    { name: "Rahul", salary: 50000 }

## Type Alias vs Interface

-   Type aliases can describe many kinds of types.
-   Interfaces are mainly used to describe object structures.
-   Both are commonly used.

# TS Union Types

## Simple Explanation

Union types allow a variable to store more than one type.

### Syntax

``` typescript
let id: string | number;

id = 101;
console.log(id);

id = "EMP101";
console.log(id);
```

Output

    101
    EMP101

# TS Functions

## Simple Explanation

TypeScript lets us define the type of function parameters and return
values.

### Syntax

``` typescript
function add(a: number, b: number): number {
  return a + b;
}

console.log(add(10, 20));
```

Output

    30

Function with no return value

``` typescript
function greet(name: string): void {
  console.log("Hello " + name);
}

greet("Deepthi");
```

Output

    Hello Deepthi

Optional Parameter

``` typescript
function introduce(name: string, city?: string) {
  console.log(name, city);
}

introduce("Deepthi");
```

Output

    Deepthi undefined

Default Parameter

``` typescript
function welcome(name: string = "Guest") {
  console.log(name);
}

welcome();
```

Output

    Guest

# TS Casting

## Simple Explanation

Casting tells TypeScript to treat a value as a specific type.

### Syntax

``` typescript
let value: unknown = "Hello";

let text = value as string;

console.log(text.length);
```

Output

    5

Alternative Syntax

``` typescript
let value: unknown = "TypeScript";

console.log((<string>value).length);
```

Output

    10

# Quick Revision

-   Objects store related data.
-   Enums represent fixed sets of values.
-   Type aliases create reusable custom types.
-   Interfaces describe object structures.
-   Union types allow multiple possible types.
-   Functions can have typed parameters and return values.
-   Casting tells TypeScript how to treat a value.
