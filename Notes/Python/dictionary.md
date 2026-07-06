
## What is a Dictionary?

A dictionary is a data structure used to store data in **key-value pairs**. Instead of using indexes like a list, we use a **key** to access its value.

A simple real-life example is an English dictionary. We search for a word (key) to get its meaning (value). Python dictionaries work in a similar way.

### Key Points

* Stores data as **key-value pairs**.
* Keys must be unique.
* Values can be repeated.
* Values can be of any data type.
* Dictionaries are mutable, so we can change them after creating them.

## Creating a Dictionary

A dictionary is created using curly braces `{}`.

### Syntax

```python
dictionary_name = {
    key1: value1,
    key2: value2
}
```

### Example

```python
student = {
    "name": "Deepthi",
    "age": 22,
    "course": "Python"
}

print(student)
```

**Output**

```
{'name': 'Deepthi', 'age': 22, 'course': 'Python'}
```

## Accessing Values

There are two common ways to access values from a dictionary.

### Using Square Brackets `[]`

Use square brackets when you're sure the key exists.

### Syntax

```python
dictionary[key]
```

### Example

```python
student = {
    "name": "Deepthi",
    "age": 22
}

print(student["name"])
```

**Output**

```
Deepthi
```

> If the key is not present, Python raises a **KeyError**.

### Using `get()`

`get()` is a safer way to access values. If the key doesn't exist, it simply returns `None` instead of showing an error.

### Syntax

```python
dictionary.get(key)
```

### Example

```python
student = {
    "name": "Deepthi"
}

print(student.get("name"))
print(student.get("age"))
```

**Output**

```
Deepthi
None
```

## Changing a Value

If a key already exists, we can change its value by assigning a new value.

### Syntax

```python
dictionary[key] = new_value
```

### Example

```python
student = {
    "name": "Deepthi",
    "age": 22
}

student["age"] = 23

print(student)
```

**Output**

```
{'name': 'Deepthi', 'age': 23}
```

## Adding a New Item

To add a new item, simply create a new key and assign a value to it.

### Syntax

```python
dictionary[new_key] = value
```

### Example

```python
student = {
    "name": "Deepthi"
}

student["course"] = "Python"

print(student)
```

**Output**

```
{'name': 'Deepthi', 'course': 'Python'}
```

## Removing Items

Python provides different ways to remove data from a dictionary.

### `pop()`

Removes the specified key.

#### Syntax

```python
dictionary.pop(key)
```

#### Example

```python
student = {
    "name": "Deepthi",
    "age": 22
}

student.pop("age")

print(student)
```

**Output**

```
{'name': 'Deepthi'}
```

### `popitem()`

Removes the last inserted key-value pair.

#### Syntax

```python
dictionary.popitem()
```

#### Example

```python
student = {
    "name": "Deepthi",
    "age": 22
}

student.popitem()

print(student)
```

**Output**

```
{'name': 'Deepthi'}
```

### `clear()`

Removes everything from the dictionary.

#### Syntax

```python
dictionary.clear()
```

#### Example

```python
student = {
    "name": "Deepthi",
    "age": 22
}

student.clear()

print(student)
```

**Output**

```
{}
```

## Looping Through a Dictionary

Looping helps us read every key or value one by one.

### Print Only the Keys

By default, a dictionary loop gives only the keys.

```python
student = {
    "name": "Deepthi",
    "age": 22,
    "course": "Python"
}

for key in student:
    print(key)
```

**Output**

```
name
age
course
```

### Print Only the Values

```python
student = {
    "name": "Deepthi",
    "age": 22,
    "course": "Python"
}

for key in student:
    print(student[key])
```

**Output**

```
Deepthi
22
Python
```

### Using `keys()`

If you only need the keys, use `keys()`.

```python
student = {
    "name": "Deepthi",
    "age": 22
}

for key in student.keys():
    print(key)
```

**Output**

```
name
age
```

### Using `values()`

If you only need the values, use `values()`.

```python
student = {
    "name": "Deepthi",
    "age": 22
}

for value in student.values():
    print(value)
```

**Output**

```
Deepthi
22
```

### Using `items()`

If you need both the key and value together, `items()` is the best choice.

```python
student = {
    "name": "Deepthi",
    "age": 22
}

for key, value in student.items():
    print(key, value)
```

**Output**

```
name Deepthi
age 22
```

## Copying a Dictionary

Sometimes we need another dictionary with the same data without changing the original one. In that case, we can use `copy()`.

### Syntax

```python
new_dictionary = dictionary.copy()
```

### Example

```python
student = {
    "name": "Deepthi"
}

new_student = student.copy()

print(new_student)
```

**Output**

```
{'name': 'Deepthi'}
```

## Dictionary Comprehension

Dictionary comprehension is a shorter way of creating dictionaries. It does the same job as a loop but in a single line.

### Syntax

```python
{key: value for item in iterable}
```

### Example

```python
square = {x: x * x for x in range(1, 6)}

print(square)
```

**Output**

```
{1: 1, 2: 4, 3: 9, 4: 16, 5: 25}
```

### Example with Condition

```python
even_square = {x: x * x for x in range(1, 11) if x % 2 == 0}

print(even_square)
```

**Output**

```
{2: 4, 4: 16, 6: 36, 8: 64, 10: 100}
```

## Nested Dictionaries

### What is a Nested Dictionary?

A nested dictionary is simply a dictionary inside another dictionary. It helps us group related information together.

### Syntax

```python
dictionary = {
    key: {
        nested_key: value
    }
}
```

### Example

```python
students = {
    "student1": {
        "name": "Deepthi",
        "age": 22
    },
    "student2": {
        "name": "Rahul",
        "age": 21
    }
}

print(students)
```

**Output**

```
{
    'student1': {'name': 'Deepthi', 'age': 22},
    'student2': {'name': 'Rahul', 'age': 21}
}
```
# Dictionary Methods

Python provides many built-in methods that make working with dictionaries much easier. Instead of writing extra code, we can use these methods to access, update, copy or remove data.



## `get()`

`get()` is used to access the value of a key safely. If the key doesn't exist, it returns `None` instead of showing an error.

### Syntax

```python
dictionary.get(key)
```

### Example

```python
student = {
    "name": "Deepthi",
    "age": 22
}

print(student.get("name"))
print(student.get("course"))
```

**Output**

```
Deepthi
None
```

> Use `get()` whenever you're not sure whether a key exists.


## `keys()`

`keys()` returns all the keys in the dictionary.

### Syntax

```python
dictionary.keys()
```

### Example

```python
student = {
    "name": "Deepthi",
    "age": 22
}

print(student.keys())
```

**Output**

```
dict_keys(['name', 'age'])
```

It is commonly used while looping through a dictionary.


## `values()`

`values()` returns all the values stored in the dictionary.

### Syntax

```python
dictionary.values()
```

### Example

```python
student = {
    "name": "Deepthi",
    "age": 22
}

print(student.values())
```

**Output**

```
dict_values(['Deepthi', 22])
```



## `items()`

`items()` returns both the key and value together as pairs.

### Syntax

```python
dictionary.items()
```

### Example

```python
student = {
    "name": "Deepthi",
    "age": 22
}

print(student.items())
```

**Output**

```
dict_items([('name', 'Deepthi'), ('age', 22)])
```

This method is very useful when you need both the key and its value while looping.



## `copy()`

`copy()` creates another dictionary with the same data.

### Syntax

```python
dictionary.copy()
```

### Example

```python
student = {
    "name": "Deepthi"
}

new_student = student.copy()

print(new_student)
```

**Output**

```
{'name': 'Deepthi'}
```



## `setdefault()`

`setdefault()` checks whether a key already exists.

* If the key exists, it returns its value.
* If the key doesn't exist, it adds the key with the given value.

### Syntax

```python
dictionary.setdefault(key, value)
```

### Example

```python
student = {
    "name": "Deepthi"
}

student.setdefault("age", 22)

print(student)
```

**Output**

```
{'name': 'Deepthi', 'age': 22}
```



## `update()`

`update()` is used to add new data or change existing data.

### Syntax

```python
dictionary.update({key: value})
```

### Example

```python
student = {
    "name": "Deepthi"
}

student.update({"age": 22})

print(student)
```

**Output**

```
{'name': 'Deepthi', 'age': 22}
```

Another example:

```python
student.update({"age": 23})

print(student)
```

**Output**

```
{'name': 'Deepthi', 'age': 23}
```



## `pop()`

`pop()` removes the specified key and returns its value.

### Syntax

```python
dictionary.pop(key)
```

### Example

```python
student = {
    "name": "Deepthi",
    "age": 22
}

student.pop("age")

print(student)
```

**Output**

```
{'name': 'Deepthi'}
```


## `popitem()`

`popitem()` removes the last inserted key-value pair.

### Syntax

```python
dictionary.popitem()
```

### Example

```python
student = {
    "name": "Deepthi",
    "age": 22,
    "course": "Python"
}

student.popitem()

print(student)
```

**Output**

```
{'name': 'Deepthi', 'age': 22}
```

## `clear()`

`clear()` removes every item from the dictionary, making it empty.

### Syntax

```python
dictionary.clear()
```

### Example

```python
student = {
    "name": "Deepthi",
    "age": 22
}

student.clear()

print(student)
```

**Output**

```
{}
```

# Quick Revision

| Operation                         | Method                        |
| --------------------------------- | ----------------------------- |
| Create a dictionary               | `{}`                          |
| Access a value                    | `[]`                          |
| Safe access                       | `get()`                       |
| Change a value                    | `dictionary[key] = value`     |
| Add a new item                    | `dictionary[new_key] = value` |
| Remove one item                   | `pop()`                       |
| Remove last item                  | `popitem()`                   |
| Remove all items                  | `clear()`                     |
| Get all keys                      | `keys()`                      |
| Get all values                    | `values()`                    |
| Get keys and values               | `items()`                     |
| Copy a dictionary                 | `copy()`                      |
| Add a key if missing              | `setdefault()`                |
| Add or update data                | `update()`                    |
| Create dictionary in one line     | Dictionary Comprehension      |
| Store a dictionary inside another | Nested Dictionary             |

# Common Mistakes

### 1. Duplicate Keys

```python
student = {
    "name": "Deepthi",
    "name": "Rahul"
}

print(student)
```

**Output**

```
{'name': 'Rahul'}
```

The latest value replaces the previous one because keys must be unique.



### 2. Accessing a Missing Key

```python
student = {
    "name": "Deepthi"
}

print(student["age"])
```

This gives a **KeyError**.

A safer option is:

```python
print(student.get("age"))
```

Output

```
None
```



### 3. Forgetting That Dictionaries Are Unordered (Conceptually)

A dictionary stores data using keys, so we should access values using their keys instead of thinking about positions or indexes.

# When Should I Use a Dictionary?

A dictionary is a good choice when:

* You want to store data as **key-value pairs**.
* Every item has a unique name or ID.
* You need fast access to values using a key.
* The data is related, like student details, employee records or product information.

Examples:

* Student details
* Employee information
* Contact list
* Product details
* Configuration settings

# Key Takeaways

* A dictionary stores data as **key-value pairs**.
* Keys are unique, but values can be repeated.
* Dictionaries are mutable.
* Use `get()` for safe access.
* Use `keys()`, `values()` and `items()` while looping.
* `update()` can add new data or change existing data.
* `pop()` removes a specific item.
* `popitem()` removes the last inserted item.
* `clear()` removes everything.
* Dictionary comprehension helps create dictionaries in a shorter way.
* Nested dictionaries are useful for storing grouped or structured data.

# Interview Tip

A question that is asked very often is:

**Dictionary vs List**

| Dictionary                | List                          |
| ------------------------- | ----------------------------- |
| Stores key-value pairs    | Stores ordered values         |
| Access using keys         | Access using indexes          |
| Keys are unique           | Duplicate values are allowed  |
| Best for searching by key | Best for storing ordered data |

> **Remember:** If your data has a meaningful key (like `name`, `id`, or `email`), a dictionary is usually the better choice. If you just need an ordered collection of values, use a list.
