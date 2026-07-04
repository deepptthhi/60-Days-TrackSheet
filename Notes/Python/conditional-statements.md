

## What is a Conditional Statement?

A **conditional statement** is used to make decisions in a program.

Python has two Boolean values:

- `True`
- `False`

It checks whether a condition is **True** or **False** and executes different blocks of code based on the result.

### Example

```python
age = 20

if age >= 18:
    print("Eligible to vote")
```

**Output**

```text
Eligible to vote
```
## Flow of a Conditional Statement

```text
Condition
    │
    ▼
Is condition True?
     │
  ┌──┴──┐
 Yes    No
  │      │
  ▼      ▼
Run    Skip / Run
Code   else block
```


# Comparison Operators

Comparison operators compare two values and return either True or False. Conditional statements use this result to decide whether to execute a block of code.

| Operator | Meaning |
|----------|---------|
| `==` | Equal to |
| `!=` | Not equal to |
| `>` | Greater than |
| `<` | Less than |
| `>=` | Greater than or equal to |
| `<=` | Less than or equal to |

> **Note:** A condition doesn't always need a comparison operator. Any value that evaluates to `True` or `False` can be used in a conditional statement.

# 1. if Statement

## What is it?

Runs a block of code **only if the condition is True**.

## Syntax

```python
if condition:
    # code
```

## Example

```python
marks = 85

if marks >= 35:
    print("Pass")
```

**Output**

```text
Pass
```

## Edge Case

If the condition is **False**, nothing inside the `if` block runs.

```python
marks = 20

if marks >= 35:
    print("Pass")

print("Program End")
```

**Output**

```text
Program End
```



# 2. if-else Statement

## What is it?

Used when there are **two possible outcomes**.

- If the condition is True → `if` block runs.
- Otherwise → `else` block runs.

## Syntax

```python
if condition:
    # code
else:
    # code
```

## Example

```python
age = 16

if age >= 18:
    print("Can vote")
else:
    print("Cannot vote")
```

**Output**

```text
Cannot vote
```

## Edge Case

Only **one block** executes.

```python
age = 20

if age >= 18:
    print("Adult")
else:
    print("Minor")
```

**Output**

```text
Adult
```


# 3. if-elif-else Statement

## What is it?

Used when there are **multiple conditions**.

Python checks conditions from top to bottom and executes the **first True** condition.

## Syntax

```python
if condition1:
    # code
elif condition2:
    # code
else:
    # code
```

## Example

```python
marks = 75

if marks >= 90:
    print("Grade A")
elif marks >= 75:
    print("Grade B")
elif marks >= 35:
    print("Pass")
else:
    print("Fail")
```

**Output**

```text
Grade B
```

## Edge Case

The order of conditions matters.

```python
marks = 95

if marks >= 35:
    print("Pass")
elif marks >= 90:
    print("Grade A")
```

**Output**

```text
Pass
```

**Why?**

The first condition is already True, so Python skips the remaining conditions.


# 4. Nested if Statement

## What is it?

A **nested if** is an `if` statement inside another `if` statement.

The inner `if` is checked **only if** the outer `if` is True.

## Syntax

```python
if condition1:
    if condition2:
        # code
```

## Example

```python
age = 22
has_id = True

if age >= 18:
    if has_id:
        print("Entry allowed")
```

**Output**

```text
Entry allowed
```

## Edge Case

If the outer condition is False, then the inner condition is never checked.

```python
age = 16
has_id = True

if age >= 18:
    if has_id:
        print("Entry allowed")

print("Done")
```

**Output**

```text
Done
```


# 5. Shorthand if Statement

## What is it?

A shorter way to write an `if` statement when there is **only one statement** to execute.

## Syntax

```python
if condition: statement
```

## Example

```python
age = 20

if age >= 18: print("Adult")
```

**Output**

```text
Adult
```

## Edge Case

Works well for simple statements only.

Not recommended:

```python
if age >= 18: print("Adult"); print("Welcome")
```

Better:

```python
if age >= 18:
    print("Adult")
    print("Welcome")
```


# 6. Shorthand if-else Statement (Ternary Operator)

## What is it?

A one line way to write an `if-else` statement.

## Syntax

```python
value_if_true if condition else value_if_false
```

## Example

```python
age = 16

result = "Adult" if age >= 18 else "Minor"

print(result)
```

**Output**

```text
Minor
```

Another example:

```python
a = 20
b = 10

print("A is bigger") if a > b else print("B is bigger")
```

**Output**

```text
A is bigger
```

## Edge Case

Avoid nested ternary operators because they are difficult to read.

Hard to read:

```python
result = "A" if x > 90 else "B" if x > 75 else "C"
```

Better:

```python
if x > 90:
    result = "A"
elif x > 75:
    result = "B"
else:
    result = "C"
```



# Special Cases 

## 1. Using `and`

All conditions must be **True**.

```python
age = 20
citizen = True

if age >= 18 and citizen:
    print("Eligible")
```

**Output**

```text
Eligible
```


## 2. Using `or`

At least **one condition** must be True.

```python
marks = 90
sports = False

if marks >= 90 or sports:
    print("Scholarship")
```

**Output**

```text
Scholarship
```



## 3. Using `not`

Reverses the result.

```python
logged_in = False

if not logged_in:
    print("Please login")
```

**Output**

```text
Please login
```



## 4. Truthy and Falsy Values

In Python, some values are automatically treated as True or False when used in an if statement.

Values treated as **False** are called **Falsy values**.

Falsy values:

- `False`
- `0`
- `0.0`
- `""` (empty string)
- `[]` (empty list)
- `{}` (empty dictionary)
- `()` (empty tuple)
- `None`

### Example

Falsy values 

```python
name = ""

if name:
    print("Name exists")
else:
    print("Name is empty")
```

**Output**

```text
Name is empty
```
Truthy values

```python
age = 20

if age:
    print("Age exists")
```
**Output**

```text
Age exists
```


> **Notes**

> - Every `if`, `elif`, and `else` statement ends with a **colon (`:`)**.
> - Python uses **indentation** (spaces) to define code blocks.
> - Every condition evaluates to either **True** or **False**.
> - In an `if-elif-else` chain, only the **first matching condition** executes.
> - Keep conditions simple and readable.
> - Use shorthand `if` and ternary operators only for simple logic.

# Easy way to remember 

| Statement | Simple Meaning |
|-----------|----------------|
| `if` | Runs code only when the condition is **True**. |
| `if-else` | Chooses between **two options**. |
| `if-elif-else` | Chooses from **multiple options**. |
| `nested if` | Checks another condition **inside an `if` block**. |
| `shorthand if` | A shorter way to write a simple `if` statement. |
| `shorthand if-else` | A shorter way to write a simple `if-else` statement in one line. |