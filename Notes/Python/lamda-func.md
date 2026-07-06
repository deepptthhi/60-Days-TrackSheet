
## What is a Lambda Function?

A lambda function is a small function that can be written in a single line.

Unlike a normal function, we don't use the `def` keyword or give it a function name. Lambda functions are mostly used when we need a simple function for a short task.

## Why Do We Use Lambda Functions?

Sometimes creating a complete function using `def` feels unnecessary, especially when the function is used only once.

In those situations, a lambda function helps us write the same logic in a shorter and cleaner way.

## Syntax

```python
lambda arguments: expression
```

* `lambda` → Keyword used to create a lambda function.
* `arguments` → Input values.
* `expression` → The operation to perform. The result is returned automatically.

## Example 1: Add Two Numbers

```python
add = lambda a, b: a + b

print(add(10, 20))
```

**Output**

```text
30
```

Here, the lambda function adds two numbers and returns the result.

## Example 2: Find the Square of a Number

```python
square = lambda x: x * x

print(square(5))
```

**Output**

```text
25
```

Instead of writing a separate function, we can do the same thing in one line.

## Lambda with `map()`

`map()` applies a function to every element in a collection.

It is useful when we want to perform the same operation on all the values.

### Syntax

```python
map(function, iterable)
```

### Example

```python
numbers = [1, 2, 3, 4]

square = list(map(lambda x: x * x, numbers))

print(square)
```

**Output**

```text
[1, 4, 9, 16]
```

Every number in the list is squared.

## Lambda with `filter()`

`filter()` returns only the values that satisfy a condition.

### Syntax

```python
filter(function, iterable)
```

### Example

```python
numbers = [1, 2, 3, 4, 5, 6]

even = list(filter(lambda x: x % 2 == 0, numbers))

print(even)
```

**Output**

```text
[2, 4, 6]
```

Only the even numbers are kept.

## Lambda with `sorted()`

A lambda function can also be used to decide how data should be sorted.

### Example

```python
students = [
    ("Deepthi", 22),
    ("Rahul", 20),
    ("Anu", 21)
]

students.sort(key=lambda x: x[1])

print(students)
```

**Output**

```text
[('Rahul', 20), ('Anu', 21), ('Deepthi', 22)]
```

Here, the list is sorted based on age instead of the names.

## Lambda vs Normal Function

### Normal Function

```python
def square(x):
    return x * x

print(square(5))
```

### Lambda Function

```python
square = lambda x: x * x

print(square(5))
```

Both produce the same output. The difference is that a lambda function is shorter and is mainly used for simple tasks.

## When Should I Use a Lambda Function?

A lambda function is a good choice when:

* The function is small and simple.
* The function is needed only once.
* You're using `map()`, `filter()`, or `sorted()`.

If the logic becomes longer or harder to understand, it's usually better to write a normal function using `def`.

## Common Mistakes

### Trying to write multiple statements

```python
lambda x:
    x + 1
```

This gives an error because a lambda function can contain only **one expression**.

### Using Lambda for Everything

Lambda functions are meant for short tasks. If the function becomes long, using a normal function makes the code much easier to read.

## Quick Revision

| Concept         | Description                               |
| --------------- | ----------------------------------------- |
| Lambda Function | A small anonymous function                |
| `lambda`        | Keyword used to create a lambda function  |
| Arguments       | Input values passed to the function       |
| Expression      | The operation performed by the function   |
| `map()`         | Applies a function to every element       |
| `filter()`      | Returns elements that satisfy a condition |
| `sorted()`      | Sorts data using a custom key             |

## Key Takeaways

* A lambda function is a short function written in a single line.
* It doesn't need the `def` keyword or a function name.
* It automatically returns the result of the expression.
* It is useful for small and simple tasks.
* Lambda functions are commonly used with `map()`, `filter()`, and `sorted()`.
* For bigger tasks, a normal function is usually easier to understand and maintain.
