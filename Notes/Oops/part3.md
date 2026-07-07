# Part 3: Advanced OOP's

So far, we've learned the fundamentals of OOP and some of its core concepts like inheritance, polymorphism, and encapsulation.

In this part, we'll learn some advanced OOP features that are commonly used in Python. These features make our classes more powerful and help us write cleaner, more Pythonic code.

# Class Methods

So far, all the methods we've written have worked with individual objects.

Sometimes, however, we want a method that works with the **class itself** instead of a particular object.

This is where **class methods** are useful.

A class method uses the `@classmethod` decorator.

Instead of `self`, it takes `cls` as its first parameter.

`cls` refers to the class itself.

## Syntax

```python
class ClassName:

    @classmethod
    def method_name(cls):
        pass
```

## Example

```python
class Student:

    college = "BIT"

    @classmethod
    def show_college(cls):
        print(cls.college)
```

Call the method.

```python
Student.show_college()
```

Output

```text
BIT
```

Notice that we called the method using the class name.

No object was created.

## When Should You Use Class Methods?

Use class methods when:

- The method works with class attributes.
- The method doesn't need data from a particular object.
- You want to create alternative constructors.

# Static Methods

Sometimes we need a method that doesn't use either the object or the class.

In such cases, we use a **static method**.

A static method uses the `@staticmethod` decorator.

It doesn't take `self` or `cls`.

## Syntax

```python
class ClassName:

    @staticmethod
    def method_name():
        pass
```

## Example

```python
class Calculator:

    @staticmethod
    def add(a, b):
        return a + b
```

Call it.

```python
Calculator.add(5, 3)
```

Output

```text
8
```

The method belongs to the class,

but it doesn't depend on the class or the object.

## When Should You Use Static Methods?

Use them when the method:

- Doesn't need object data.
- Doesn't need class data.
- Is related to the class but works like a helper function.

# Instance Method vs Class Method vs Static Method

| Feature | Instance Method | Class Method | Static Method |
|----------|-----------------|--------------|---------------|
| First Parameter | `self` | `cls` | None |
| Works With | Object | Class | Neither |
| Needs Object? | Yes | No | No |
| Decorator | None | `@classmethod` | `@staticmethod` |

# Magic (Dunder) Methods

You may have noticed methods like:

```python
__init__()
```

These are called **Magic Methods** or **Dunder (Double Underscore) Methods**.

Python automatically calls these methods at different times.

They help us customize how our objects behave.

# `__str__()`

Normally,

if we print an object,

Python shows something like this.

```text
<__main__.Student object at 0x000001>
```

That isn't very useful.

Using `__str__()`, we can control what gets printed.

## Example

```python
class Student:

    def __init__(self, name):
        self.name = name

    def __str__(self):
        return self.name
```

Now,

```python
student = Student("Deepthi")

print(student)
```

Output

```text
Deepthi
```

# `__repr__()`

`__repr__()` is similar to `__str__()`.

The difference is:

- `__str__()` is for users.
- `__repr__()` is mainly for developers.

If `__str__()` is not available,

Python automatically uses `__repr__()`.

Example

```python
class Student:

    def __repr__(self):
        return "Student Object"
```

# `__len__()`

This method tells Python what should happen when we use `len()`.

Example

```python
class Book:

    def __len__(self):
        return 250
```

Now,

```python
book = Book()

len(book)
```

Output

```text
250
```

# `__eq__()`

This method tells Python how two objects should be compared.

Example

```python
class Student:

    def __init__(self, marks):
        self.marks = marks

    def __eq__(self, other):
        return self.marks == other.marks
```

Now,

```python
s1 = Student(90)
s2 = Student(90)

print(s1 == s2)
```

Output

```text
True
```

Without `__eq__()`,

Python would compare their memory locations instead.

# `__new__()`

Whenever an object is created,

Python actually performs two steps.

```
Step 1 → __new__()

Step 2 → __init__()
```

`__new__()` creates the object.

`__init__()` initializes it.

Most Python programmers never need to override `__new__()`.

Just remember:

> **`__new__()` creates the object.**
>
> **`__init__()` prepares the object.**

# Object Lifecycle

Every object goes through a simple lifecycle.

```
Class Created
      ↓
Object Created (__new__)
      ↓
Initialized (__init__)
      ↓
Used in Program
      ↓
Destroyed Automatically
```

Python automatically removes objects from memory when they are no longer needed.

This process is called **Garbage Collection**.

# Garbage Collection

Memory is limited.

Python automatically frees the memory used by objects that are no longer being used.

This process is called **Garbage Collection**.

The programmer usually doesn't need to manage memory manually.

That's one of the advantages of Python.

# Best Practices

Here are a few good habits while writing OOP code.

- Give classes meaningful names.
- Give methods meaningful names.
- Keep methods short.
- Don't repeat code.
- Use inheritance only when needed.
- Prefer composition when classes are only loosely related.
- Keep data private whenever possible.
- Write one class for one responsibility.

# Composition (Basic Idea)

Sometimes,

instead of inheriting another class,

one class simply **contains** another class.

This is called **Composition**.

Example:

```python
class Engine:

    def start(self):
        print("Engine Started")

class Car:

    def __init__(self):
        self.engine = Engine()
```

Here,

a car **has an** engine.

It is not an engine.

Whenever you hear:

> **Has-A Relationship**

think of **Composition**.

Whenever you hear:

> **Is-A Relationship**

think of **Inheritance**.

# Common Beginner Mistakes

## Using Inheritance Everywhere

Not every class should inherit another class.

Sometimes composition is a better choice.

## Writing Large Classes

Avoid putting everything inside one class.

Instead,

divide responsibilities into smaller classes.

## Ignoring Encapsulation

Don't allow every variable to be modified directly.

Use methods whenever validation is needed.

## Forgetting Magic Methods

Magic methods make objects easier to use.

Learn the commonly used ones like:

- `__init__()`
- `__str__()`
- `__repr__()`
- `__len__()`
- `__eq__()`

# Quick Revision

- Class methods work with the class.
- Static methods work independently.
- Magic methods customize object behavior.
- `__str__()` controls printing.
- `__repr__()` is mainly for developers.
- `__len__()` works with `len()`.
- `__eq__()` compares objects.
- `__new__()` creates objects.
- `__init__()` initializes objects.
- Python automatically manages memory using Garbage Collection.
- Composition represents a **Has-A** relationship.
- Inheritance represents an **Is-A** relationship.

# One-Line Summary

Object-Oriented Programming helps us organize code into reusable, maintainable, and scalable classes. By understanding classes, objects, inheritance, polymorphism, encapsulation, methods, and Python's special features like magic methods and composition, you now have a strong foundation to build real-world Python applications.
