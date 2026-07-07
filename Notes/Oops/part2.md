# Part 2: Core OOP's

## Inheritance & Code Reusability

In Part 1, we learned how to create classes and objects. We also learned how objects store data and perform actions using methods.

Now let's learn one of the biggest advantages of OOP—**Inheritance**.

Inheritance allows one class to use the properties and methods of another class. Instead of writing the same code again and again, we can simply inherit it and add only what is new.

# What is Inheritance?

Inheritance is a feature in OOP where one class acquires the properties and methods of another class.

In simple words, a child class can reuse the code of a parent class.

Think about a family.

A child inherits many features from their parents, like eye color or hair color.

Similarly, a child class inherits attributes and methods from a parent class.

This saves time and avoids writing duplicate code.

# Why Do We Use Inheritance?

Without inheritance, we often end up writing the same code multiple times.

Imagine creating classes for:

- Student
- Teacher
- Employee

All of them have:

- Name
- Age
- Address

Instead of writing these attributes in every class, we can create one parent class and let the others inherit from it.

This makes the code:

- Cleaner
- Shorter
- Easier to maintain
- Easier to update

# Parent Class

A **parent class** is the class whose properties and methods are inherited by another class.

It is also called:

- Base Class
- Superclass

Example:

```python
class Animal:

    def eat(self):
        print("Animal is eating")
```

Here,

`Animal` is the parent class.

# Child Class

A **child class** inherits everything from the parent class.

It is also called:

- Derived Class
- Subclass

Syntax:

```python
class ChildClass(ParentClass):
    pass
```

Example:

```python
class Animal:

    def eat(self):
        print("Animal is eating")

class Dog(Animal):
    pass
```

Here,

`Dog` inherits from `Animal`.

Even though `Dog` has no methods of its own, it can still use the `eat()` method.

```python
dog = Dog()
dog.eat()
```

Output

```text
Animal is eating
```

The method belongs to `Animal`, but `Dog` can use it because of inheritance.

# Adding New Features to the Child Class

A child class is not limited to the parent's methods.

It can also have its own methods.

Example:

```python
class Animal:

    def eat(self):
        print("Animal is eating")

class Dog(Animal):

    def bark(self):
        print("Woof!")
```

Now,

```python
dog = Dog()

dog.eat()
dog.bark()
```

Output

```text
Animal is eating
Woof!
```

The child class now has:

- The parent's method (`eat()`)
- Its own method (`bark()`)

# Method Overriding

Sometimes the parent already has a method, but the child wants to perform the same action differently.

This is called **Method Overriding**.

Example:

```python
class Animal:

    def speak(self):
        print("Some generic animal sound")

class Dog(Animal):

    def speak(self):
        print("Woof!")
```

Now,

```python
dog = Dog()
dog.speak()
```

Output

```text
Woof!
```

Python uses the child's version of the method instead of the parent's version.

This is called **overriding** because the child replaces the parent's implementation.

# Why Override a Method?

Every animal can speak, but not every animal makes the same sound.

Instead of creating different method names like:

```python
dog_sound()
cat_sound()
lion_sound()
```

we simply use

```python
speak()
```

Each child class decides how it wants to implement it.

This makes the code cleaner and easier to understand.

# `super()`

Sometimes we don't want to completely replace the parent's method.

Instead, we want to use the parent's method first and then add our own code.

For this, Python provides the `super()` function.

Example:

```python
class Animal:

    def speak(self):
        print("Animal makes a sound")

class Dog(Animal):

    def speak(self):
        super().speak()
        print("Woof!")
```

Now,

```python
dog = Dog()
dog.speak()
```

Output

```text
Animal makes a sound
Woof!
```

The parent's method runs first.

Then the child's code runs.

# Why Do We Use `super()`?

Imagine the parent method already does something useful.

Instead of writing that code again, we simply call it.

This helps us:

- Reuse existing code
- Reduce duplication
- Keep programs easier to maintain

# Using `super()` with Constructors

`super()` is commonly used inside constructors.

Example:

```python
class Person:

    def __init__(self, name):
        self.name = name

class Student(Person):

    def __init__(self, name, roll_no):
        super().__init__(name)
        self.roll_no = roll_no
```

Create an object.

```python
student = Student("Deepthi", 101)
```

Now,

```
student.name
```

comes from the parent class.

```
student.roll_no
```

comes from the child class.

Without `super()`, we would have to write the parent's initialization code again.

# Constructor Inheritance

If the child class doesn't have its own constructor, Python automatically uses the parent's constructor.

Example:

```python
class Animal:

    def __init__(self):
        print("Animal Constructor")

class Dog(Animal):
    pass

dog = Dog()
```

Output

```text
Animal Constructor
```

Since `Dog` doesn't define its own constructor, Python uses the parent's constructor.

# Constructor Overriding

If the child creates its own constructor, the parent's constructor is no longer called automatically.

Example:

```python
class Animal:

    def __init__(self):
        print("Animal Constructor")

class Dog(Animal):

    def __init__(self):
        print("Dog Constructor")

dog = Dog()
```

Output

```text
Dog Constructor
```

If we also want the parent's constructor to run, we must use `super()`.

```python
class Dog(Animal):

    def __init__(self):
        super().__init__()
        print("Dog Constructor")
```

Output

```text
Animal Constructor
Dog Constructor
```

# Method Resolution Order (MRO)

Sometimes a class can inherit from multiple classes.

Python follows a fixed order to decide which method should be called first.

This order is called the **Method Resolution Order (MRO)**.

You don't need to memorize it now.

Just remember:

> Python always follows a specific order while searching for methods.

You can check the order using:

```python
ClassName.mro()
```

or

```python
help(ClassName)
```

# Real-Life Example of Inheritance

Imagine a company.

Every employee has:

- Name
- Employee ID
- Salary

Instead of writing these details separately for every role, we create one parent class.

```python
Employee
```

Then we create:

```text
Manager
Developer
Tester
HR
```

All these classes automatically get the common details from `Employee`.

Each one can also have its own unique methods.

For example,

```text
Developer → write_code()

Manager → conduct_meeting()

Tester → test_application()
```

This is exactly how inheritance works in real projects.

# Common Beginner Mistakes

## Forgetting Parent Class Name

Wrong

```python
class Dog:
    pass
```

Correct

```python
class Dog(Animal):
    pass
```

## Writing Duplicate Code

If multiple classes have the same attributes or methods, move them into a parent class instead of copying them.

## Forgetting `super()`

If the parent constructor contains important initialization, remember to call it using:

```python
super().__init__()
```

Otherwise, the parent's constructor won't run.

# Quick Revision

- Inheritance allows one class to reuse another class's code.
- The parent class is also called the superclass.
- The child class is also called the subclass.
- Child classes inherit attributes and methods from the parent.
- Method overriding allows a child class to replace a parent's method.
- `super()` is used to access the parent class.
- Constructors can also be inherited.
- MRO decides the order in which Python searches for methods.

# One-Line Summary

Inheritance helps us write cleaner, shorter, and reusable code by allowing child classes to use and extend the features of parent classes.

## Polymorphism, Encapsulation & Inner Classes

In the previous section, we learned how one class can inherit another class using inheritance.

Now let's look at three more important OOP concepts that make our code flexible, secure, and easier to manage.

These concepts are:

- Polymorphism
- Encapsulation
- Inner (Nested) Classes

# What is Polymorphism?

The word **Polymorphism** comes from two Greek words:

- **Poly** → Many
- **Morph** → Forms

In programming, polymorphism means:

> **The same method name can behave differently for different objects.**

Think about a TV remote.

Every TV has a **Power** button.

Whether it's Samsung, Sony, or LG, you press the same button.

But each TV turns on in its own way.

The button is the same.

The behavior is different.

That's exactly what polymorphism means.

# Example

```python
class Dog:

    def speak(self):
        print("Woof!")

class Cat:

    def speak(self):
        print("Meow!")

class Cow:

    def speak(self):
        print("Moo!")
```

Now,

```python
animals = [Dog(), Cat(), Cow()]

for animal in animals:
    animal.speak()
```

Output

```text
Woof!
Meow!
Moo!
```

Notice something.

We never checked

```python
if animal == Dog
```

or

```python
if animal == Cat
```

We simply called

```python
animal.speak()
```

Each object knew what it should do.

That's polymorphism.

# Why Do We Use Polymorphism?

Without polymorphism, our code would be full of conditions like this.

```python
if animal == "Dog":
    ...
elif animal == "Cat":
    ...
elif animal == "Cow":
    ...
```

Instead,

every object handles its own work.

This makes programs:

- Cleaner
- Easier to extend
- Easier to maintain

# Duck Typing (Basic Idea)

Python follows a concept called **Duck Typing**.

You may have heard this sentence.

> "If it walks like a duck and quacks like a duck, treat it as a duck."

In Python, we don't always care about the object's type.

We only care whether it has the method we want.

Example:

```python
class Dog:

    def speak(self):
        print("Woof!")

class Human:

    def speak(self):
        print("Hello!")
```

Now,

```python
def make_sound(obj):
    obj.speak()
```

Call it.

```python
make_sound(Dog())
make_sound(Human())
```

Output

```text
Woof!
Hello!
```

Python never checks whether the object is a Dog or a Human.

It only checks whether the object has a

```python
speak()
```

method.

This is called Duck Typing.

# What is Encapsulation?

Encapsulation means keeping **data and the methods that work on that data together inside one class.**

It also means protecting the data from being changed in the wrong way.

Think about a bank account.

Imagine anyone could write

```python
balance = -50000
```

That wouldn't make sense.

Instead,

the bank provides methods like:

- Deposit
- Withdraw

These methods check whether the operation is valid before changing the balance.

That's encapsulation.

# Example

```python
class BankAccount:

    def __init__(self, balance):
        self.balance = balance

    def deposit(self, amount):
        self.balance += amount

    def withdraw(self, amount):

        if amount <= self.balance:
            self.balance -= amount

        else:
            print("Insufficient Balance")
```

Now,

```python
account = BankAccount(1000)

account.withdraw(500)
```

works correctly.

Instead of changing

```python
balance
```

directly,

we let the methods control the changes.

# Why Do We Use Encapsulation?

Encapsulation helps us:

- Protect data
- Prevent invalid changes
- Keep related code together
- Make programs easier to maintain

# Public Members

By default,

every variable and method in Python is **public**.

That means anyone can access it.

Example

```python
class Student:

    def __init__(self):
        self.name = "Deepthi"
```

Now,

```python
student = Student()

print(student.name)
```

Output

```text
Deepthi
```

Public members can be accessed from anywhere.

# Protected Members

Protected members start with a single underscore.

Example

```python
class Student:

    def __init__(self):
        self._age = 21
```

Python doesn't stop you from accessing it.

```python
print(student._age)
```

still works.

The underscore is simply a message to other programmers.

It means

> "This should only be used inside the class or its child classes."

It's a convention, not a rule.

# Private Members

Private members start with two underscores.

Example

```python
class Student:

    def __init__(self):
        self.__marks = 95
```

Now,

```python
print(student.__marks)
```

gives an error.

Python hides the variable using **Name Mangling**.

# Name Mangling

Python changes

```python
__marks
```

into something like

```python
_Student__marks
```

internally.

That's why

```python
student.__marks
```

doesn't work.

But

```python
student._Student__marks
```

does.

Although this is possible,

it's generally not recommended.

Private variables are meant to be accessed only inside the class.

# Why Does Python Use Name Mangling?

The main purpose is to avoid accidental modification.

It is **not** meant to provide complete security.

# Inner (Nested) Classes

Sometimes one class is closely related to another class.

Instead of creating them separately,

we can place one class inside another.

This is called an **Inner Class** or **Nested Class**.

# Example

```python
class Car:

    class Engine:

        def start(self):
            print("Engine Started")

    def __init__(self):
        self.engine = self.Engine()
```

Now,

```python
car = Car()

car.engine.start()
```

Output

```text
Engine Started
```

Here,

the `Engine` class only makes sense as part of a `Car`.

That's why it's placed inside the `Car` class.

# When Should We Use Inner Classes?

Inner classes are useful when:

- One class only belongs to another class.
- We want better code organization.
- The inner class doesn't need to be used independently.

They are not very common in everyday Python programming,

but it's good to know they exist.

# Common Beginner Mistakes

## Thinking Polymorphism Needs Inheritance

It doesn't.

Different classes can have the same method name without inheriting from each other.

## Accessing Private Variables Directly

Wrong

```python
student.__marks
```

Correct

Access the data using methods whenever possible.

## Forgetting That Protected Members Are Only a Convention

A single underscore doesn't make a variable truly private.

It simply tells other programmers,

"Please don't access this directly."

## Overusing Inner Classes

Not every helper class should be nested.

Use inner classes only when the relationship is very strong.

# Quick Revision

- Polymorphism means one method can have different behaviors.
- Duck Typing focuses on what an object can do, not what it is.
- Encapsulation keeps data and methods together.
- Public members can be accessed anywhere.
- Protected members use one underscore (`_`).
- Private members use two underscores (`__`).
- Name Mangling changes private variable names internally.
- Inner classes are classes defined inside another class.

# One-Line Summary

Polymorphism makes code flexible, encapsulation protects data, and inner classes help organize closely related classes.
