

## What is JSON?

JSON stands for **JavaScript Object Notation**.

Even though it has "JavaScript" in its name, it is used in many programming languages, including Python.

You can think of JSON as a simple way of storing and sharing data. It is commonly used when different applications need to exchange information, such as websites, mobile apps, and APIs.

## Why Do We Use JSON?

JSON is useful because it helps us:

* Store data in a simple format.
* Share data between different applications.
* Send and receive data from APIs.
* Save structured data in files.

## Importing the JSON Module

Before working with JSON, we need to import Python's built-in `json` module.

### Syntax

```python
import json
```

## Python Dictionary vs JSON

When I first saw JSON, it looked almost the same as a Python dictionary.

The main difference is that a dictionary is a Python object, while JSON is just a text format used to store or transfer data.

| Python Dictionary               | JSON                           |
| ------------------------------- | ------------------------------ |
| Python object                   | Text format                    |
| Can use single or double quotes | Uses only double quotes        |
| Used inside Python programs     | Used to exchange or store data |

## Converting a Python Object to JSON

The `dumps()` function converts a Python object into a JSON string.

### Syntax

```python
json.dumps(object)
```

### Example

```python
import json

student = {
    "name": "Deepthi",
    "age": 22
}

result = json.dumps(student)

print(result)
```

**Output**

```text
{"name": "Deepthi", "age": 22}
```

Here, the Python dictionary is converted into JSON.

## Converting JSON to a Python Object

The `loads()` function converts a JSON string into a Python object.

### Syntax

```python
json.loads(json_string)
```

### Example

```python
import json

student = '{"name":"Deepthi","age":22}'

result = json.loads(student)

print(result)
print(type(result))
```

**Output**

```text
{'name': 'Deepthi', 'age': 22}
<class 'dict'>
```

The JSON data is converted back into a Python dictionary.

## Writing JSON to a File

If we want to save JSON data in a file, we use the `dump()` function.

### Syntax

```python
json.dump(object, file)
```

### Example

```python
import json

student = {
    "name": "Deepthi",
    "age": 22
}

with open("student.json", "w") as file:
    json.dump(student, file)
```

This creates a file called **student.json** and stores the data in JSON format.

## Reading JSON from a File

To read JSON data from a file, we use the `load()` function.

### Syntax

```python
json.load(file)
```

### Example

```python
import json

with open("student.json", "r") as file:
    data = json.load(file)

print(data)
```

**Output**

```text
{'name': 'Deepthi', 'age': 22}
```

The JSON data is converted into a Python dictionary, so we can work with it easily.

## Formatting JSON

Sometimes JSON appears on a single line, which makes it difficult to read.

Using the `indent` parameter makes the output much cleaner.

### Example

```python
import json

student = {
    "name": "Deepthi",
    "age": 22,
    "course": "Python"
}

print(json.dumps(student, indent=4))
```

**Output**

```text
{
    "name": "Deepthi",
    "age": 22,
    "course": "Python"
}
```

## Common Mistakes

### Forgetting to Import the Module

```python
json.dumps({"name": "Deepthi"})
```

This gives an error because Python doesn't know what `json` is.

The correct way is:

```python
import json

json.dumps({"name": "Deepthi"})
```

### Confusing `dump()` and `dumps()`

This confused me when I first learned JSON.

The easiest way I remember it is:

* `dump()` → Writes JSON to a **file**.
* `dumps()` → Converts a Python object into a **JSON string**.

Similarly,

* `load()` → Reads JSON from a **file**.
* `loads()` → Reads JSON from a **string**.

## Quick Revision

| Concept       | Description                                 |
| ------------- | ------------------------------------------- |
| JSON          | A format used to store and exchange data    |
| `import json` | Imports the JSON module                     |
| `dumps()`     | Converts a Python object into a JSON string |
| `loads()`     | Converts a JSON string into a Python object |
| `dump()`      | Writes JSON to a file                       |
| `load()`      | Reads JSON from a file                      |
| `indent`      | Makes JSON output easier to read            |

## Key Takeaways

* JSON is a simple format used to store and exchange data.
* Python provides the built-in `json` module to work with JSON.
* `dumps()` converts Python objects into JSON strings.
* `loads()` converts JSON strings into Python objects.
* `dump()` writes JSON data to a file.
* `load()` reads JSON data from a file.
* Using `indent` makes JSON much easier to read.
