# Variables

A **variable** is used to store data. Think of it as a box that holds a value.

## Creating Variables

In Python, you don't need to declare a variable first. Just assign a value to it.

```python
name = "Deepthi"
age = 21

print(name)
print(age)
```


## Variables Can Change

A variable can store different types of values.

```python
x = 10
x = "Python"

print(x)
```


## Check the Data Type

Use `type()` to check the data type of a variable.

```python
name = "Deepthi"

print(type(name))
```


## Variable Naming Rules

Valid variable names

```python
name
my_age
studentName
_marks
```

Invalid variable names

```python
2name
my-name
my name
```

> **Remember:**
 - Start with a letter or `_`
 - Don't start with a number
 - No spaces or special characters (except `_`)
 - Variable names are **case-sensitive** (`age` and `Age` are different)


## Naming Styles

```python
# Snake Case (Most common in Python)
student_name

# Camel Case
studentName

# Pascal Case
StudentName
```

> **Tip:** Use **snake_case** while writing Python code.


## Assigning Multiple Variables

Assign different values:

```python
x, y, z = 10, 20, 30
```

Assign the same value:

```python
x = y = z = 100
```


## Output Variables

Print multiple variables using commas.

```python
name = "Deepthi"
age = 21

print(name, age)
```

> **Note:** Using commas lets you print different data types together without any errors.