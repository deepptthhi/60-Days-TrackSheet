# Advanced Types



# TS Advanced Types

## Simple Explanation

Advanced types help us create flexible and reusable code while still keeping type safety.

Example

``` typescript
type ID = string | number;

let userId: ID = 101;
console.log(userId);

userId = "EMP101";
console.log(userId);
```

Output

    101
    EMP101

# TS Type Guards

## Simple Explanation

Type guards help TypeScript figure out the exact type of a variable before using it.

### Using typeof

``` typescript
function print(value: string | number) {
  if (typeof value === "string") {
    console.log(value.toUpperCase());
  } else {
    console.log(value * 2);
  }
}

print("hello");
print(10);
```

Output

    HELLO
    20

# TS Conditional Types

## Simple Explanation

Conditional types choose one type or another based on a condition.

### Syntax

``` typescript
type Check<T> = T extends string ? "Text" : "Not Text";

type A = Check<string>;
type B = Check<number>;
```

Output

    A = "Text"
    B = "Not Text"

# TS Mapped Types

## Simple Explanation

Mapped types create new types by modifying existing ones.

### Example

``` typescript
type Student = {
  name: string;
  age: number;
};

type ReadOnlyStudent = {
  readonly [K in keyof Student]: Student[K];
};
```

Now all properties become read-only.

# TS Type Inference

## Simple Explanation

Type inference means TypeScript automatically understands the type without you writing it.

### Example

``` typescript
let name = "Deepthi";
let age = 22;
```

TypeScript understands:

``` typescript
name: string
age: number
```

Output

    Deepthi
    22

# TS Literal Types

## Simple Explanation

Literal types allow only specific values.

### Example

``` typescript
let direction: "left" | "right";

direction = "left";
console.log(direction);
```

Output

    left

Wrong Example

``` typescript
direction = "up";
```

Output

    Error

Literal types are useful when only a few values are allowed.

# When are these used?

-   Type Guards → Checking user input
-   Conditional Types → Building reusable libraries
-   Mapped Types → Updating existing types
-   Type Inference → Writing cleaner code
-   Literal Types → Restricting valid values

# Quick Revision

-   Advanced types make TypeScript more flexible.
-   Type guards safely identify data types.
-   Conditional types choose a type based on a condition.
-   Mapped types transform existing types.
-   Type inference lets TypeScript guess types.
-   Literal types allow only fixed values.
