

## Input (`input()`)

The `input()` function is used to take input from the user.

### Basic Input

```python
name = input("Enter your name: ")
print("Hello,", name)
```

**Output**

```
Enter your name: Deepthi
Hello, Deepthi
```

### Multiple Inputs

You can take input more than once.

```python
name = input("Enter your name: ")
age = input("Enter your age: ")

print(name, age)
```

### Input is Always a String

Even if the user enters a number, `input()` stores it as a string.

```python
age = input("Enter your age: ")
print(type(age))
```

**Output**

```
<class 'str'>
```

### Converting Input

Use `int()` or `float()` when you need a number.

```python
age = int(input("Enter your age: "))
height = float(input("Enter your height: "))
```

## Output (`print()`)

The `print()` function is used to display output on the screen.

### Print Text

```python
print("Hello, World!")
```

### Print Numbers

```python
print(10)
print(5 + 5)
```

### Print Text and Numbers

```python
age = 21
print("Age:", age)
```

### Print on the Same Line

```python
print("Hello", end=" ")
print("World!")
```

**Output**

```
Hello World!
```

> **Remember**
> - `input()` → Takes input from the user.
> - `print()` → Displays output on the screen.
> - Text → Use quotes (`" "` or `' '`).
> - Numbers → No quotes needed.
> - `input()` always returns a string. Use `int()` or `float()` if you need a number.