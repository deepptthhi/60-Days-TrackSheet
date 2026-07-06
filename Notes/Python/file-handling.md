

## What is File Handling?

File handling is the process of working with files in Python.

Normally, the data inside a program is lost once the program finishes running. If we want to save that data and use it later, we need files.

Python makes it easy to create files, read data from them, write new data, update existing data, and even delete files when they are no longer needed.

## Why Do We Use File Handling?

File handling helps us:

* Read data from a file.
* Write data into a file.
* Create new files.
* Add new content without removing the old content.
* Save information for later use.
* Delete files that are no longer needed.

## Opening a File

Before we can read or write a file, we first need to open it.

Python provides the `open()` function for this.

### Syntax

```python
open(file_name, mode)
```

### Example

```python
file = open("sample.txt", "r")
```

Here,

* `"sample.txt"` is the file name.
* `"r"` tells Python that we want to read the file.

## File Modes

Different modes are used depending on what we want to do.

| Mode  | Purpose                                                       |
| ----- | ------------------------------------------------------------- |
| `"r"` | Read a file                                                   |
| `"w"` | Write to a file (creates a new file if it doesn't exist)      |
| `"a"` | Add new content to the end of a file                          |
| `"x"` | Create a new file (gives an error if the file already exists) |

## Reading a File

### `read()`

The `read()` method reads the entire file.

```python
file = open("sample.txt", "r")

print(file.read())

file.close()
```

**Output**

```text
Hello
Welcome to Python
```

This is useful when the file is small and we want to read everything at once.

## Reading One Line

### `readline()`

The `readline()` method reads only one line at a time.

```python
file = open("sample.txt", "r")

print(file.readline())

file.close()
```

**Output**

```text
Hello
```

If we call `readline()` again, it reads the next line.

## Reading All Lines

### `readlines()`

The `readlines()` method returns every line as a list.

```python
file = open("sample.txt", "r")

print(file.readlines())

file.close()
```

**Output**

```text
['Hello\n', 'Welcome to Python']
```

This is helpful when we want to work with each line separately.

## Reading a File Using a Loop

Instead of reading the whole file at once, we can go through it one line at a time.

```python
file = open("sample.txt", "r")

for line in file:
    print(line)

file.close()
```

I found this approach easier to understand because it reads the file step by step. It's also a better choice when working with large files.

## Writing to a File

The `"w"` mode is used to write data into a file.

If the file doesn't exist, Python creates it.

If the file already exists, all the old content is removed and replaced with the new content.

```python
file = open("sample.txt", "w")

file.write("Hello Python")

file.close()
```

## Appending to a File

Sometimes we don't want to remove the existing content. We only want to add something new.

For that, we use the `"a"` mode.

```python
file = open("sample.txt", "a")

file.write("\nLearning File Handling")

file.close()
```

The new text is added at the end of the file without changing the old content.

## Creating a New File

The `"x"` mode is used to create a new file.

If the file already exists, Python shows an error.

```python
file = open("notes.txt", "x")

file.close()
```

## Closing a File

After finishing our work, it's a good habit to close the file.

```python
file.close()
```

Closing a file makes sure all the changes are saved properly and frees the resources used by the file.

## Using the `with` Statement

Instead of calling `close()` ourselves, we can use the `with` statement.

Python automatically closes the file after the work is finished.

```python
with open("sample.txt", "r") as file:
    print(file.read())
```

I found this much easier because I don't have to remember to close the file manually.

## Deleting a File

To delete a file, we use the `os` module.

```python
import os

os.remove("sample.txt")
```

Before deleting a file, it's a good idea to check if it exists.

```python
import os

if os.path.exists("sample.txt"):
    os.remove("sample.txt")
```

This avoids getting an error if the file is already missing.

## Common Mistakes

### Forgetting to Close the File

```python
file = open("sample.txt", "r")

print(file.read())
```

The program works, but it's better to close the file after using it.

A better approach is:

```python
with open("sample.txt", "r") as file:
    print(file.read())
```

Python closes the file automatically.

### Using the Wrong File Mode

This confused me at first.

If we open a file using `"w"`, all the existing content is removed.

So before opening a file, it's always worth checking whether we want to:

* Read the file (`"r"`)
* Replace the content (`"w"`)
* Add new content (`"a"`)

## Quick Revision

| Method / Mode | Purpose                                 |
| ------------- | --------------------------------------- |
| `open()`      | Opens a file                            |
| `"r"`         | Reads a file                            |
| `"w"`         | Writes to a file                        |
| `"a"`         | Adds data to the end of a file          |
| `"x"`         | Creates a new file                      |
| `read()`      | Reads the entire file                   |
| `readline()`  | Reads one line                          |
| `readlines()` | Reads all lines as a list               |
| `write()`     | Writes data to a file                   |
| `close()`     | Closes the file                         |
| `with open()` | Opens and closes the file automatically |
| `os.remove()` | Deletes a file                          |

## Key Takeaways

* File handling lets us save data so it can be used later.
* Always open a file before reading or writing.
* Choose the correct file mode depending on what you want to do.
* `with open()` is the easiest and safest way to work with files.
* Close the file if you're not using the `with` statement.
* Check whether a file exists before deleting it.
