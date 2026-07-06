

## What is a Module?

A module is simply a Python file that contains code we can use in other programs. It can contain functions, variables, classes, or any Python code.

Instead of writing the same code every time, we can write it once inside a module and import it whenever we need it. This keeps the code cleaner and saves time.

Python also provides many built-in modules, so we can use them directly instead of writing everything ourselves.

## Why Do We Use Modules?

Modules are useful because they help us:

* Keep our code organized.
* Reuse the same code in different programs.
* Make programs easier to read and maintain.
* Use Python's built-in features without writing them from scratch.

## Importing a Module

To use a module, we use the `import` keyword.

### Syntax

```python
import module_name
```

### Example

```python
import math

print(math.sqrt(25))
```

**Output**

```text
5.0
```

Here, we imported the `math` module and used its `sqrt()` function to find the square root of a number.

## Importing a Specific Function

Sometimes we don't need the whole module. We may only need one or two functions. In that case, we can import only those functions.

### Syntax

```python
from module_name import function_name
```

### Example

```python
from math import sqrt

print(sqrt(49))
```

**Output**

```text
7.0
```

Since we imported `sqrt()` directly, we don't have to write `math.sqrt()`.

## Importing Multiple Functions

We can also import more than one function from the same module.

### Syntax

```python
from module_name import function1, function2
```

### Example

```python
from math import sqrt, factorial

print(sqrt(16))
print(factorial(5))
```

**Output**

```text
4.0
120
```

## Using an Alias

Sometimes module names are long, or we just want to type less. We can give a module another name using the `as` keyword.

### Syntax

```python
import module_name as alias
```

### Example

```python
import math as m

print(m.pi)
print(m.sqrt(36))
```

**Output**

```text
3.141592653589793
6.0
```

Using an alias makes the code shorter and a little easier to read.

## The `dir()` Function

When I first saw a module, I wondered how to know what functions were available inside it. That's where `dir()` is useful.

It shows all the functions, variables, and other objects available in a module.

### Syntax

```python
dir(module_name)
```

### Example

```python
import math

print(dir(math))
```

**Output**

```text
['acos', 'asin', 'atan', 'ceil', 'cos', 'factorial', ...]
```

The output is long because it lists everything available in that module.

## The `help()` Function

If we want to know how a module or function works, we can use `help()`.

It shows the documentation directly inside Python.

### Syntax

```python
help(module_name)
```

### Example

```python
import math

help(math)
```

The output contains information about the `math` module and all the functions available in it.

## Creating Your Own Module

We can also create our own modules.

Suppose we create a file called **greetings.py**.

### greetings.py

```python
def welcome(name):
    return "Welcome " + name
```

Now we can use that function in another Python file.

```python
import greetings

print(greetings.welcome("Deepthi"))
```

**Output**

```text
Welcome Deepthi
```

This is useful because we can write the code once and use it in different programs whenever we need it.

## Some Common Built-in Modules

Python provides many built-in modules. Some of the ones I'll probably use often are:

| Module     | Purpose                       |
| ---------- | ----------------------------- |
| `math`     | Mathematical calculations     |
| `random`   | Generate random numbers       |
| `datetime` | Work with dates and time      |
| `os`       | Work with files and folders   |
| `json`     | Read and write JSON data      |
| `re`       | Work with regular expressions |

## Note

A module must be imported before it can be used.

If Python doesn't know where the module is, it will show an error.

## Common Mistakes

### Forgetting to Import the Module

```python
print(math.sqrt(25))
```

**Output**

```text
NameError
```

Correct way:

```python
import math

print(math.sqrt(25))
```

### Forgetting the Module Name

```python
import math

print(sqrt(25))
```

**Output**

```text
NameError
```

Correct way:

```python
print(math.sqrt(25))
```

or

```python
from math import sqrt

print(sqrt(25))
```

## Quick Revision

| Concept           | Description                                     |
| ----------------- | ----------------------------------------------- |
| Module            | A Python file that contains reusable code       |
| `import`          | Imports a module                                |
| `from ... import` | Imports specific functions                      |
| `as`              | Gives a module another name                     |
| `dir()`           | Shows everything inside a module                |
| `help()`          | Displays information about a module or function |

## Key Takeaways

* A module is a Python file that contains reusable code.
* Modules help avoid writing the same code again and again.
* Use `import` to use an entire module.
* Use `from ... import` when you only need specific functions.
* Use `as` to give a module a shorter name.
* `dir()` helps us explore a module.
* `help()` helps us understand how a module or function works.
* Python provides many built-in modules, and we can also create our own.
