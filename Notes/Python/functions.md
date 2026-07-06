# Python Functions

## What is a Function?

A function is a block of code that performs a specific task. Instead of writing the same code again and again, we can write it once inside a function and use it whenever we need it.

Think of a function like a machine. We give it some input, it performs a task, and gives us the required output.

### Why Do We Use Functions?

Functions help us:

* Avoid writing the same code multiple times.
* Make programs easier to read.
* Break a large problem into smaller parts.
* Reuse code whenever needed.
* Make debugging and updating code easier.

## Types of Functions

Python mainly has two types of functions.

### 1. Built-in Functions

These are functions that Python already provides. We can use them directly without creating them.

Some common built-in functions are:

* `print()`
* `input()`
* `len()`
* `type()`
* `max()`
* `min()`
* `sum()`
* `abs()`
* `round()`

### Example

```python
print("Hello")
print(len("Python"))
print(max(10, 25, 15))
print(type(10))
```

**Output**

```text
Hello
6
25
<class 'int'>
```

### 2. User-defined Functions

These are functions that we create ourselves using the `def` keyword.

Whenever the built-in functions are not enough, we can create our own function based on our requirements.

### Example

```python
def greet():
    print("Hello")

greet()
```

**Output**

```text
Hello
```

## Defining a Function

A function is created using the `def` keyword.

### Syntax

```python
def function_name():
    # code
```

### Example

```python
def welcome():
    print("Welcome to Python")

welcome()
```

**Output**

```text
Welcome to Python
```

## Calling a Function

Creating a function doesn't run it.

A function runs only when we call it using its name followed by parentheses.

### Syntax

```python
function_name()
```

### Example

```python
def greet():
    print("Good Morning")

greet()
greet()
```

**Output**

```text
Good Morning
Good Morning
```

The same function can be called as many times as we want.

## Function Without Parameters

A function without parameters doesn't take any input from the user.

### Syntax

```python
def function_name():
    # code
```

### Example

```python
def message():
    print("Learning Python")

message()
```

**Output**

```text
Learning Python
```

## Function With Parameters

A function with parameters accepts input while it is running. This allows the same function to work with different values.

### Syntax

```python
def function_name(parameter):
    # code
```

### Example

```python
def greet(name):
    print("Hello", name)

greet("Deepthi")
```

**Output**

```text
Hello Deepthi
```

## Parameters

A parameter is a variable written inside the function definition. It acts like a placeholder that receives a value when the function is called.

### Syntax

```python
def function_name(parameter):
    # code
```

### Example

```python
def student(name):
    print(name)

student("Deepthi")
```

Here, `name` is the **parameter**.

**Output**

```text
Deepthi
```

## Arguments

An argument is the actual value that we pass while calling a function. The parameter receives this value.

### Syntax

```python
function_name(argument)
```

### Example

```python
def student(name):
    print(name)

student("Deepthi")
```

Here, `"Deepthi"` is the **argument**.

**Output**

```text
Deepthi
```

## Difference Between Parameters and Arguments

| Parameter                         | Argument                           |
| --------------------------------- | ---------------------------------- |
| Written while defining a function | Passed while calling a function    |
| Acts as a placeholder             | Actual value given to the function |
| Receives the value                | Sends the value                    |

## Types of Arguments

Python supports different ways of passing arguments.

### 1. Positional Arguments

The values are passed in the same order as the parameters.

### Example

```python
def student(name, age):
    print(name, age)

student("Deepthi", 22)
```

**Output**

```text
Deepthi 22
```

### 2. Keyword Arguments

Instead of depending on the order, we specify the parameter names.

### Example

```python
def student(name, age):
    print(name, age)

student(age=22, name="Deepthi")
```

**Output**

```text
Deepthi 22
```

The order doesn't matter because the parameter names are mentioned.

### 3. Default Arguments

A parameter can have a default value. If no argument is passed, Python automatically uses the default value.

### Example

```python
def greet(name="Guest"):
    print("Hello", name)

greet()
greet("Deepthi")
```

**Output**

```text
Hello Guest
Hello Deepthi
```

### 4. Variable-Length Arguments (`*args`)

Sometimes we don't know how many values will be passed to a function. `*args` allows a function to accept multiple positional arguments.

### Syntax

```python
def function_name(*args):
    # code
```

### Example

```python
def numbers(*values):
    print(values)

numbers(10, 20, 30, 40)
```

**Output**

```text
(10, 20, 30, 40)
```

`*args` stores all the values as a tuple.

# Return Statement

The `return` statement is used to send a value back from a function.

Unlike `print()`, which only displays the result on the screen, `return` gives the result back so it can be stored in a variable or used later in the program.

## Why Do We Use `return`?

We use `return` when we want to:

* Get a value back from a function.
* Store the result in a variable.
* Use the result in another calculation.
* Make functions more reusable.

## Syntax

```python
def function_name():
    return value
```

### Example

```python
def add(a, b):
    return a + b

result = add(10, 20)

print(result)
```

**Output**

```text
30
```

Here, the function returns `30`, which is stored in the variable `result`.

## Returning Multiple Values

A function can also return more than one value.

### Example

```python
def student():
    return "Deepthi", 22

name, age = student()

print(name)
print(age)
```

**Output**

```text
Deepthi
22
```

## `return` Ends the Function

Once Python reaches a `return` statement, the function stops executing.

### Example

```python
def message():
    print("Hello")
    return
    print("Welcome")

message()
```

**Output**

```text
Hello
```

The second `print()` is never executed because the function has already returned.

# Difference Between `print()` and `return`

Many beginners confuse these two, but they are used for different purposes.

| `print()`                                     | `return`                                                      |
| --------------------------------------------- | ------------------------------------------------------------- |
| Displays the output on the screen             | Sends a value back from the function                          |
| Cannot be reused later                        | Can be stored in a variable                                   |
| Mainly used for testing or displaying results | Mainly used when another part of the program needs the result |

### Example using `print()`

```python
def add(a, b):
    print(a + b)

add(5, 3)
```

**Output**

```text
8
```

The value is displayed, but we cannot use it later.

### Example using `return`

```python
def add(a, b):
    return a + b

result = add(5, 3)

print(result)
print(result * 2)
```

**Output**

```text
8
16
```

Since the function returns a value, we can use it again whenever we want.

# Variable Scope

Scope decides where a variable can be accessed in a program.

Python mainly has two types of variables.

## Local Variable

A local variable is created inside a function.

It can only be used inside that function.

### Example

```python
def student():
    name = "Deepthi"
    print(name)

student()
```

**Output**

```text
Deepthi
```

Trying to access `name` outside the function gives an error.

```python
print(name)
```

**Output**

```text
NameError
```

## Global Variable

A global variable is created outside a function.

It can be accessed both inside and outside the function.

### Example

```python
name = "Deepthi"

def student():
    print(name)

student()

print(name)
```

**Output**

```text
Deepthi
Deepthi
```

# Common Mistakes

## 1. Forgetting to Call the Function

Creating a function does not run it.

```python
def greet():
    print("Hello")
```

Nothing will happen until we call it.

```python
greet()
```



## 2. Forgetting the Parentheses

```python
def greet():
    print("Hello")

greet
```

Here, the function is not called.

The correct way is:

```python
greet()
```



## 3. Passing the Wrong Number of Arguments

```python
def add(a, b):
    return a + b

add(10)
```

**Output**

```text
TypeError
```

The function expects two arguments, but only one is given.



## 4. Confusing Parameters and Arguments

```python
def student(name):
    print(name)

student("Deepthi")
```

* `name` → Parameter
* `"Deepthi"` → Argument



## 5. Using `print()` Instead of `return`

Many beginners use `print()` when they actually need `return`.

If the value needs to be used later, always use `return`.

# When Should I Use Functions?

Functions are useful when:

* The same code is repeated many times.
* A large program needs to be divided into smaller parts.
* You want your code to be clean and easy to understand.
* The same task needs to be used in different places.

# Quick Revision

| Concept             | Purpose                                      |
| ------------------- | -------------------------------------------- |
| `def`               | Creates a function                           |
| Function Call       | Runs the function                            |
| Parameter           | Placeholder inside a function                |
| Argument            | Actual value passed to the function          |
| Positional Argument | Passed based on order                        |
| Keyword Argument    | Passed using parameter name                  |
| Default Argument    | Uses a default value if no argument is given |
| `*args`             | Accepts multiple positional arguments        |
| `return`            | Sends a value back from a function           |
| Local Variable      | Accessible only inside the function          |
| Global Variable     | Accessible throughout the program            |

# Key Takeaways

* A function is a reusable block of code.
* Functions make programs shorter, cleaner, and easier to maintain.
* `def` is used to create a function.
* A function runs only when it is called.
* Parameters receive values from arguments.
* Arguments are the actual values passed while calling a function.
* `return` sends a value back from the function.
* `print()` only displays the result.
* Local variables exist only inside a function.
* Global variables can be accessed throughout the program.
* `*args` allows a function to accept multiple values.

# Interview Tip

A common interview question is:

**Function vs Method**

| Function               | Method                     |
| ---------------------- | -------------------------- |
| Can be called directly | Belongs to an object       |
| Example: `print()`     | Example: `name.upper()`    |
| Works independently    | Works on a specific object |

> **Remember:** Every method is a function, but not every function is a method. A method is simply a function that belongs to an object.
