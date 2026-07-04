

## What is a Loop?

A **loop** is used to repeat a block of code multiple times.

Instead of writing the same code again and again, we use a loop to perform repetitive tasks automatically.

### Example

```python
for i in range(3):
    print("Hello")
```

**Output**

```text
Hello
Hello
Hello
```


## Flow of a Loop

```text
Start
   │
   ▼
Check Condition
   │
 ┌─┴─┐
 │   │
Yes  No
 │    │
 ▼    ▼
Execute End
 Code
 │
 ▼
Repeat
```


# Types of Loops

Python has two main types of loops:

- `for` loop
- `while` loop

A special form of the `while` loop is:

- `while True`

Loops can also be placed inside another loop. This is called a **nested loop**.

# 1. for Loop

## What is it?

A **for loop** repeats a block of code for every item in a sequence.

It's useful when you already know how many times the loop should run.

## Syntax

```python
for variable in sequence:
    # code
```

## Example

```python
for i in range(1, 6):
    print(i)
```

**Output**

```text
1
2
3
4
5
```

## Edge Case

If the sequence is empty, the loop does not execute.

```python
for i in []:
    print(i)

print("Done")
```

**Output**

```text
Done
```


# 2. while Loop

## What is it?

A **while loop** repeats a block of code as long as the given condition is **True**.

It's useful when we do not know how many times the loop should run.

## Syntax

```python
while condition:
    # code
```

## Example

```python
count = 1

while count <= 5:
    print(count)
    count += 1
```

**Output**

```text
1
2
3
4
5
```

## Edge Case

If the condition is **False** from the beginning, the loop never executes.

```python
count = 10

while count <= 5:
    print(count)

print("Done")
```

**Output**

```text
Done
```

# 3. while True Loop

## What is it?

`while True` creates an **infinite loop** because the condition is always **True**.

It keeps running until it is stopped manually or by using the `break` statement.

## Syntax

```python
while True:
    # code
```

## Example

```python
count = 1

while True:
    print(count)

    if count == 5:
        break

    count += 1
```

**Output**

```text
1
2
3
4
5
```

## Edge Case

If there is no `break` statement or another way to stop the loop, it runs forever.

```python
while True:
    print("Hello")
```

This creates an **infinite loop**.



# Nested Loop

## What is it?

A **nested loop** is a loop inside another loop.

For every iteration of the outer loop, the inner loop runs completely.

## Syntax

```python
for variable1 in sequence:
    for variable2 in sequence:
        # code
```

## Example

```python
for i in range(1, 3):
    for j in range(1, 4):
        print(i, j)
```

**Output**

```text
1 1
1 2
1 3
2 1
2 2
2 3
```

## Edge Case

Nested loops increase the number of iterations, so they can become slow when working with large amounts of data.


# range()

## What is it?

`range()` is a built-in Python function that generates a sequence of numbers.

It is commonly used with `for` loops.


## Syntax

```python
range(stop)

range(start, stop)

range(start, stop, step)
```


## 1. range(stop)

Starts from **0** and ends before **stop**.

### Example

```python
for i in range(5):
    print(i)
```

**Output**

```text
0
1
2
3
4
```

## 2. range(start, stop)

Starts from **start** and ends before **stop**.

### Example

```python
for i in range(2, 6):
    print(i)
```

**Output**

```text
2
3
4
5
```

## 3. range(start, stop, step)

Moves by the given **step** value.

### Example

```python
for i in range(2, 11, 2):
    print(i)
```

**Output**

```text
2
4
6
8
10
```

## Edge Cases

### Using a negative step

```python
for i in range(5, 0, -1):
    print(i)
```

**Output**

```text
5
4
3
2
1
```

### If the range has no values

```python
for i in range(5, 5):
    print(i)

print("Done")
```

**Output**

```text
Done
```


# Basic Programming Concepts for Loops

## 1. Loop Variable

The variable used inside a loop to access each value is called the **loop variable** or **iterator**.

### Example

```python
for number in range(5):
    print(number)
```

Here, `number` is the loop variable.


## 2. Counter Variable

A counter variable keeps track of how many times something has happened.

### Example

```python
count = 1

while count <= 5:
    print(count)
    count += 1
```

Here, `count` is the counter variable.


## 3. Infinite Loop

An **infinite loop** is a loop that never ends.

### Example

```python
while True:
    print("Hello")
```

To stop it, press **Ctrl + C** or use the `break` statement.


# pass Statement

## What is it?

`pass` doesn't do anything.

It's used when Python expects code, but you don't want to write it.

## Syntax

```python
pass
```

## Example

```python
for i in range(5):
    pass

print("Loop completed")
```

**Output**

```text
Loop completed
```

## Edge Case

Without `pass`, Python gives an error if a block is empty.

Incorrect:

```python
if True:
```

Correct:

```python
if True:
    pass
```


# break Statement

## What is it?

The `break` statement is used to **stop a loop immediately**.

Once `break` is executed, Python exits the loop and continues with the next statement after the loop.

## Syntax

```python
break
```

## Example

```python
for i in range(1, 6):
    if i == 4:
        break
    print(i)
```

**Output**

```text
1
2
3
```

## Edge Case

`break` only exits the loop in which it is written.

In nested loops, it stops only the **inner loop**, not the outer loop.


# continue Statement

## What is it?

The `continue` statement skips the **current iteration** and moves to the next iteration of the loop.

It does not stop the loop.

## Syntax

```python
continue
```

## Example

```python
for i in range(1, 6):
    if i == 3:
        continue
    print(i)
```

**Output**

```text
1
2
4
5
```

## Edge Case

If `continue` is used inside a `while` loop, make sure the loop variable is updated. Otherwise, it may create an infinite loop.

Correct:

```python
count = 0

while count < 5:
    count += 1

    if count == 3:
        continue

    print(count)
```

**Output**

```text
1
2
4
5
```

# Loop with Conditional Statements

## What is it?

A loop can contain an `if`, `if-else`, or `if-elif-else` statement.

This allows the program to make decisions during each iteration of the loop.

## Syntax

```python
for variable in sequence:
    if condition:
        # code
```

## Example

```python
for number in range(1, 6):
    if number % 2 == 0:
        print(number)
```

**Output**

```text
2
4
```

## Another Example

```python
for number in range(1, 6):
    if number % 2 == 0:
        print(number, "is Even")
    else:
        print(number, "is Odd")
```

**Output**

```text
1 is Odd
2 is Even
3 is Odd
4 is Even
5 is Odd
```


# Common Mistakes

## 1. Forgetting the colon (`:`)

Incorrect:

```python
for i in range(5)
    print(i)
```

Correct:

```python
for i in range(5):
    print(i)
```


## 2. Wrong indentation

Incorrect:

```python
for i in range(5):
print(i)
```

Correct:

```python
for i in range(5):
    print(i)
```


## 3. Forgetting to update the variable in a `while` loop

Incorrect:

```python
count = 1

while count <= 5:
    print(count)
```

This creates an **infinite loop**.

Correct:

```python
count = 1

while count <= 5:
    print(count)
    count += 1
```


## 4. Using `break` when `continue` is needed

`break` stops the loop completely.

`continue` skips only the current iteration.

Choose the correct statement based on what you want the loop to do.


## 5. Using an empty block without `pass`

Incorrect:

```python
if True:
```

Correct:

```python
if True:
    pass
```


# When to use which?

| Statement | What it does |
|-----------|--------------|
| `break` | Stops the loop immediately. |
| `continue` | Skips the current iteration and moves to the next one. |
| `pass` | Leave the block empty. |

> **Things to Remember**
>
> - Loops help to avoid writing the same code again and again.
> - Use `for` when you know how many times the loop should run.
> - Use `while` when the loop depends on a condition.
> - `while True` keeps running until `break` is used.
> - `break` stops the loop.
> - `continue` skips the current iteration.
> - `pass` is used when you don't want to write the code yet.
> - Don't forget to maintain proper indentation.

# Quick Summary

| Topic | Remember it as |
|--------|-------------------|
| `for` | Repeat a fixed number of times. |
| `while` | Repeat until the condition becomes `False`. |
| `while True` | Keep running until stopped. |
| `Nested Loop` | One loop inside another. |
| `range()` | Generates numbers for a loop. |
| `break` | Stops the loop. |
| `continue` | Skips the iteration. |
| `pass` | Leave the block empty for now. |