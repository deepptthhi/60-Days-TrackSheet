

## What is a Tuple?

A **tuple** is used to store multiple values in a single variable, just like a list.

The main difference is that **tuples are immutable**, which means once a tuple is created, its elements cannot be changed, added, or removed.

Tuples are useful when the data should remain fixed throughout the program.

```python
fruits = ("Apple", "Banana", "Mango")
numbers = (10, 20, 30, 40)
mixed = ("Deepthi", 22, True)
```

## How to Create a Tuple

A tuple is created by placing elements inside **parentheses `()`**.

### Syntax

```python
tuple_name = (item1, item2, item3)
```

### Example

```python
colors = ("Red", "Green", "Blue")
```

A tuple with only one element must have a comma.

```python
fruit = ("Apple",)
```

Without the comma, Python treats it as a string.

```python
fruit = ("Apple")
```

## Tuple Indexing

Every element in a tuple has its own position called an **index**.

Indexing starts from **0**.

```python
colors = ("Red", "Green", "Blue")
```

| Element | Red | Green | Blue |
|----------|-----|-------|------|
| Index | 0 | 1 | 2 |
| Negative Index | -3 | -2 | -1 |

### Example

```python
colors = ("Red", "Green", "Blue")

print(colors[0])
print(colors[-1])
```

**Output**

```
Red
Blue
```

## Tuple Slicing

Slicing is used to get a part of a tuple.

### Syntax

```python
tuple[start:end]
```

The start index is included, but the end index is not.

### Example

```python
numbers = (10, 20, 30, 40, 50)

print(numbers[1:4])
print(numbers[:3])
print(numbers[2:])
print(numbers[::-1])
```

**Output**

```
(20, 30, 40)
(10, 20, 30)
(30, 40, 50)
(50, 40, 30, 20, 10)
```

## Iterating Through a Tuple

### Using a for Loop

The easiest way to access every element.

```python
fruits = ("Apple", "Banana", "Mango")

for fruit in fruits:
    print(fruit)
```

**Output**

```
Apple
Banana
Mango
```

## Using range() and len()

This is useful when you also need the index.

```python
fruits = ("Apple", "Banana", "Mango")

for i in range(len(fruits)):
    print(fruits[i])
```

**Output**

```
Apple
Banana
Mango
```

## Using a while Loop

```python
fruits = ("Apple", "Banana", "Mango")

i = 0

while i < len(fruits):
    print(fruits[i])
    i += 1
```

**Output**

```
Apple
Banana
Mango
```

# Tuple Functions

## len()

Returns the total number of elements.

```python
numbers = (10, 20, 30, 40)

print(len(numbers))
```

**Output**

```
4
```

## count()

Returns how many times an element appears.

```python
numbers = (1, 2, 2, 3, 2)

print(numbers.count(2))
```

**Output**

```
3
```

## index()

Returns the position of the first occurrence of an element.

```python
fruits = ("Apple", "Banana", "Mango")

print(fruits.index("Banana"))
```

**Output**

```
1
```

## max()

Returns the largest element.

```python
numbers = (10, 40, 15, 25)

print(max(numbers))
```

**Output**

```
40
```

## min()

Returns the smallest element.

```python
numbers = (10, 40, 15, 25)

print(min(numbers))
```

**Output**

```
10
```

## sum()

Returns the sum of all numeric elements.

```python
numbers = (10, 20, 30)

print(sum(numbers))
```

**Output**

```
60
```

## Conversion of Tuples

Sometimes we need to convert between a list and a tuple.

### Convert List to Tuple

```python
numbers = [10, 20, 30]

new_tuple = tuple(numbers)

print(new_tuple)
```

**Output**

```
(10, 20, 30)
```

### Convert Tuple to List

This is useful because lists can be modified.

```python
numbers = (10, 20, 30)

new_list = list(numbers)

print(new_list)
```

**Output**

```
[10, 20, 30]
```

After converting to a list, you can add, remove, or update elements.

## Why Use Tuples?

Use a tuple when:

- The data should not change.
- You want to protect data from accidental modification.
- You need slightly better performance than a list.
- You are storing fixed values like months, days, or coordinates.

Use a list when you need to add, remove, or update elements.

# Things to Remember

- Tuples store multiple values.
- Tuples are immutable.
- Tuples allow duplicate values.
- Indexing starts from **0**.
- Slicing works the same way as lists.
- Tuples support loops like `for` and `while`.
- Tuples cannot use methods like `append()`, `insert()`, `remove()`, or `pop()`.
- If you need to modify a tuple, first convert it to a list.

# Quick Summary

| Function | Purpose |
|----------|---------|
| `len()` | Returns the number of elements |
| `count()` | Counts the occurrence of an element |
| `index()` | Returns the index of an element |
| `max()` | Returns the largest element |
| `min()` | Returns the smallest element |
| `sum()` | Returns the sum of numeric elements |
| `tuple()` | Converts a list to a tuple |
| `list()` | Converts a tuple to a list |

> **NOTE**
> 
>| List | Tuple |
>|------|-------|
>| Uses **`[]`** | Uses **`()`** |
>| Can be changed (Mutable) | Cannot be changed (Immutable) |
>| Used for changing data | Used for fixed data |