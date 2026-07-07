# Part 1: Foundations & Fundamentals

Before learning advanced OOP concepts, it's important to understand the basics. Almost everything in Object-Oriented Programming is built on these concepts. Once these ideas are clear, learning the rest of OOP becomes much easier.

# What is OOP?

**OOP (Object-Oriented Programming)** is a way of writing programs by organizing code into **objects**.

An object contains:

- Data (called **attributes**)
- Functions (called **methods**)

Instead of writing everything in one place, OOP groups related data and functions together.

Think of a mobile phone.

A phone has:

- Brand
- Model
- Battery Percentage

These are its **attributes**.

A phone can also:

- Call
- Send Messages
- Take Photos

These are its **methods**.

In OOP, we try to represent real-world things in the same way.

# Why Do We Use OOP?

As programs become bigger, managing everything with normal functions becomes difficult.

OOP helps us by:

- Organizing code properly
- Reusing existing code
- Reducing repetition
- Making programs easier to read
- Making programs easier to maintain
- Making teamwork easier

Instead of writing the same code again and again, we create classes and reuse them whenever needed.

# Advantages of OOP

Some benefits of OOP are:

- Better code organization
- Code reusability
- Easier debugging
- Easier maintenance
- Better readability
- Real-world modeling
- Easy to extend existing programs

# Classes and Objects

Before writing any OOP program, you should understand these two words.

## What is a Class?

A **class** is simply a blueprint or a design.

It tells Python what an object should have and what it should be able to do.

A class itself is not a real object.

Think of it like a house blueprint.

A blueprint shows where the rooms, doors, and windows should be.

But you cannot live inside a blueprint.

Similarly, a class only defines an object.

## What is an Object?

An **object** is the actual thing created from a class.

Using one class, we can create many objects.

Every object is independent.

Think about a classroom.

There is one student registration form.

Many students fill the same form.

The form is like the class.

Each student is an object.

## Creating a Class

The `class` keyword is used to create a class.

### Syntax

```python
class ClassName:
    pass
```

### Example

```python
class Dog:
    pass
```

Here, `Dog` is a class.

## Creating Objects

Objects are created by calling the class.

```python
class Dog:
    pass

dog1 = Dog()
dog2 = Dog()
```

Now we have two different objects.

Although both come from the same class, they are stored separately in memory.

Changing one object does not affect the other.

## Class vs Object

| Class | Object |
|--------|--------|
| Blueprint | Real instance |
| Defines structure | Stores actual data |
| Created once | Can create many |
| Does not hold individual data | Holds its own data |

### Easy Way to Remember

> **Class = Blueprint**  
> **Object = Real thing created from the blueprint**

# Constructor (`__init__()`)

When we create an object, Python automatically runs a special method called `__init__()`.

This method is called the **constructor**.

Its job is to give the object its initial values.

Think about buying a new phone.

When you switch it on for the first time, it asks for:

- Language
- Wi-Fi
- Time Zone

Only after these settings is the phone ready to use.

A constructor works in the same way.

It prepares the object before we start using it.

### Syntax

```python
class Dog:

    def __init__(self, name):
        self.name = name
```

### Create an Object

```python
dog1 = Dog("Rocky")
```

Here,

```python
Dog("Rocky")
```

automatically runs

```python
__init__()
```

and stores the value `"Rocky"` inside the object.

### Why Do We Need a Constructor?

Without a constructor:

```python
class Dog:
    pass

dog1 = Dog()
```

The object has no data.

We would have to do this manually.

```python
dog1.name = "Rocky"
```

Using a constructor is much cleaner.

### Remember

A constructor automatically gives an object its starting values.

# `self`

When beginners first learn Python OOP, `self` often looks confusing.

But the idea is actually simple.

`self` means:

> **This object**

Whenever an object calls a method, Python automatically sends that object as the first argument.

We never pass `self` ourselves.

### Example

```python
class Dog:

    def __init__(self, name):
        self.name = name

    def bark(self):
        print(f"{self.name} says Woof!")
```

Create objects.

```python
dog1 = Dog("Rocky")
dog2 = Dog("Bruno")
```

Now call

```python
dog1.bark()
```

**Output**

```text
Rocky says Woof!
```

If we call

```python
dog2.bark()
```

**Output**

```text
Bruno says Woof!
```

The same method is being used.

The only difference is that `self` tells Python which object's data should be used.

### Easy Way to Remember

Whenever you see

```python
self
```

read it as

> "this object"

or simply

> "me"

# Attributes

An **attribute** is simply a variable that belongs to a class or an object.

Python has two types of attributes.

- Instance Attributes
- Class Attributes

## Instance Attributes

Instance attributes belong to individual objects.

Each object gets its own copy.

They are usually created inside the constructor.

### Example

```python
class Student:

    def __init__(self, name):
        self.name = name
```

Create objects.

```python
s1 = Student("Deepthi")
s2 = Student("Rahul")
```

Now,

```text
s1.name → Deepthi
s2.name → Rahul
```

Changing one object's name does not change the other.

Use instance attributes whenever every object should have its own value.

Examples:

- Name
- Age
- Salary
- Balance
- Roll Number

## Class Attributes

Class attributes belong to the class.

Every object shares the same value.

### Example

```python
class Student:

    college = "BIT"

    def __init__(self, name):
        self.name = name
```

Now,

```python
print(s1.college)
print(s2.college)
```

**Output**

```text
BIT
BIT
```

Both objects share the same value.

Use class attributes whenever the value is common for every object.

Examples:

- College Name
- Company Name
- Country
- Species

## Mutable Class Attributes

Be careful while using lists or dictionaries as class attributes.

### Example

```python
class Student:

    marks = []
```

Now every object shares the same list.

```python
s1.marks.append(90)
```

If we check

```python
print(s2.marks)
```

**Output**

```text
[90]
```

This happens because both objects are using the same list.

If every object should have its own list, create it inside `__init__()`.

```python
class Student:

    def __init__(self):
        self.marks = []
```

Now every object gets a different list.

## Instance Attributes vs Class Attributes

| Instance Attributes | Class Attributes |
|---------------------|------------------|
| Belong to an object | Belong to the class |
| Each object has its own copy | Shared by all objects |
| Usually created inside `__init__()` | Created directly inside the class |
| Different for every object | Usually same for every object |

# Instance Methods

Methods are simply functions written inside a class.

The most common type is an **instance method**.

Instance methods always use `self`.

They work with the data of a particular object.

### Example

```python
class BankAccount:

    def __init__(self, balance):
        self.balance = balance

    def deposit(self, amount):
        self.balance += amount

    def show_balance(self):
        print(self.balance)
```

Create an object.

```python
account = BankAccount(1000)
```

Deposit money.

```python
account.deposit(500)
```

Check the balance.

```python
account.show_balance()
```

**Output**

```text
1500
```

The method changed only this object's balance.

Another object would have its own balance.

# Properties (Basic Idea)

A property is simply a value that belongs to an object.

Examples:

A student may have:

- Name
- Age
- Roll Number

A car may have:

- Brand
- Model
- Color

These values are called properties.

In Python, we usually store them as attributes.

### Example

```python
class Car:

    def __init__(self, brand, color):
        self.brand = brand
        self.color = color
```

Now every car object stores its own brand and color.

# Common Beginner Mistakes

## Forgetting `self`

**Wrong**

```python
class Dog:

    def bark():
        print("Woof")
```

**Correct**

```python
class Dog:

    def bark(self):
        print("Woof")
```

## Forgetting `__init__()`

If you don't initialize your data, you'll have to add everything manually later.

Using a constructor makes your code much cleaner.

## Confusing Classes and Objects

Remember:

- A class is only a design.
- An object is the actual thing created from that design.

## Using Mutable Class Attributes

Avoid writing

```python
marks = []
```

unless you intentionally want every object to share the same list.

# Quick Revision

- OOP organizes code using objects.
- A class is a blueprint.
- An object is created from a class.
- `__init__()` is the constructor.
- A constructor gives an object its initial values.
- `self` refers to the current object.
- Instance attributes belong to individual objects.
- Class attributes are shared by every object.
- Instance methods work with a specific object's data.
- Properties are values stored inside an object.

# One-Line Summary

If you understand **classes, objects, constructors, `self`, attributes, and instance methods**, you've built a strong foundation for learning the rest of Object-Oriented Programming.

