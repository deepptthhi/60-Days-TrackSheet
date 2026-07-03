# Errors in Python

An **error** is a problem in a program that stops it from running correctly.

Python errors are mainly of three types:

- Syntax Errors
- Runtime Errors (Exceptions)
- Logical Errors


## 1. Syntax Error

A syntax error happens when we break Python's rules (syntax). The program won't run until the error is fixed.

### Example

```python
if 5 > 2
    print("Hello")
```

**Output**

```
SyntaxError
```
### Common Syntax Errors

### IndentationError

Python uses indentation (spaces) to define blocks of code. If the indentation is missing or incorrect, Python raises an `IndentationError`.

```python
if True:
print("Hello")
```

**Output**

```
IndentationError: expected an indented block
```


## 2. Runtime Errors (Exceptions)

A runtime error happens while the program is running. The code starts executing but stops when it encounters an error.

These errors are also called **exceptions**.

### Common Runtime Errors

### ZeroDivisionError

Occurs when a number is divided by zero.

```python
print(10 / 0)
```

### NameError

Occurs when you use a variable or function that has not been defined.

```python
print(name)
```

### TypeError

Occurs when an operation is performed on wrong  data types.

```python
print("10" + 5)
```


### ValueError

Occurs when the data type is correct, but the value is invalid.

```python
age = int("abc")
```


### IndexError

Occurs when trying to access an index that doesn't exist.

```python
numbers = [1, 2, 3]

print(numbers[5])
```

### KeyError

Occurs when a dictionary key is not found.

```python
student = {
    "name": "Deepthi"
}

print(student["age"])
```

### FileNotFoundError

Occurs when Python cannot find the file or when trying to open a file that doesn't exist.

```python
open("notes.txt", "r")
```

### AttributeError

Occurs when an object doesn't have the requested attribute or method.

```python
name = "Python"

name.append("!")
```



## 3. Logical Error

A logical error means the program runs without any error, but the output is incorrect because the logic is wrong.

### Example

```python
length = 10
breadth = 5

area = length + breadth

print(area)
```

The program runs successfully, but the formula is wrong.

Correct formula:

```python
area = length * breadth
```
> **Note** - Logical errors are the hardest to find because Python doesn't show any error message.

# Exception Handling

Sometimes errors can cause a program to stop suddenly.

Exception handling helps us to handle these errors so the program can continue running.

Python uses the following blocks for exception handling:

- `try`
- `except`
- `else`
- `finally`


## try

The code that may cause an error is written inside the `try` block.

```python
try:
    print(10 / 0)
```


## except

If an error occurs, the `except` block handles it.

```python
try:
    print(10 / 0)
except:
    print("Cannot divide by zero.")
```

## else

The `else` block runs only if no error occurs.

```python
try:
    print(10 / 2)
except:
    print("Error")
else:
    print("Program executed successfully.")
```


## finally

The `finally` block always runs, whether an error occurs or not.

```python
try:
    print(10 / 2)
except:
    print("Error")
finally:
    print("Execution completed.")
```

# Easy Way to Remember

| Error Type | Meaning |
|------------|---------|
| Syntax Error | Wrong Python syntax |
| Runtime Error | Error occurs while the program is running |
| Logical Error | Program runs but gives the wrong output |

---

## Remember

- **Syntax Error** → Program doesn't start.
- **Runtime Error** → Program starts but stops because of an exception.
- **Logical Error** → Program runs successfully but produces the wrong result.
- **Exception Handling** → Prevents the program from crashing by handling runtime errors.