

## What is a List?

A **list** is used to store multiple values in a single variable.

A list can store numbers, strings, or even different types of data together.

Unlike strings, **lists are mutable**, which means we can add, remove, or change elements whenever we want.

Lists are written inside **square brackets `[]`**.

```python
fruits = ["Apple", "Banana", "Mango"]
numbers = [10, 20, 30, 40]
mixed = ["Deepthi", 22, True]
```



# How to Create a List

A list is created by placing elements inside square brackets.

### Syntax

```python
list_name = [item1, item2, item3]
```

### Example

```python
colors = ["Red", "Green", "Blue"]
```

# List Indexing

Every element in a list has its own position called an **index**.

Indexing starts from **0**.

```python
colors = ["Red", "Green", "Blue"]
```

| Element | Red | Green | Blue |
|----------|------|--------|------|
| Index | 0 | 1 | 2 |
| Negative Index | -3 | -2 | -1 |

### Example

```python
colors = ["Red", "Green", "Blue"]

print(colors[0])
print(colors[-1])
```

**Output**

```
Red
Blue
```

# List Slicing

Slicing is used to get a part of a list.

### Syntax

```python
list[start:end]
```

The start index is included, but the end index is not.

### Example

```python
numbers = [10, 20, 30, 40, 50]

print(numbers[1:4])
print(numbers[:3])
print(numbers[2:])
print(numbers[::-1])
```

**Output**

```
[20, 30, 40]
[10, 20, 30]
[30, 40, 50]
[50, 40, 30, 20, 10]
```

# Iterating Through a List

## Using a for Loop

The simplest way to access every element.

```python
fruits = ["Apple", "Banana", "Mango"]

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

This gives access to the index as well.

```python
fruits = ["Apple", "Banana", "Mango"]

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
fruits = ["Apple", "Banana", "Mango"]

i = 0

while i < len(fruits):
    print(fruits[i])
    i += 1
```


## Shorthand for Loop

A shorter way to loop through a list.

```python
numbers = [1, 2, 3, 4]

[print(i) for i in numbers]
```



# Common List Methods

## len()

Returns the total number of elements.

```python
numbers = [10, 20, 30]

print(len(numbers))
```

**Output**

```
3
```



## count()

Returns how many times an element appears.

```python
numbers = [1, 2, 2, 3, 2]

print(numbers.count(2))
```

**Output**

```
3
```



## insert()

Adds an element at a specific position.

### Syntax

```python
list.insert(index, value)
```

### Example

```python
fruits = ["Apple", "Mango"]

fruits.insert(1, "Banana")

print(fruits)
```

**Output**

```
['Apple', 'Banana', 'Mango']
```



## append()

Adds an element at the end.

```python
fruits = ["Apple", "Banana"]

fruits.append("Orange")

print(fruits)
```

**Output**

```
['Apple', 'Banana', 'Orange']
```


## remove()

Removes a specific element.

```python
fruits = ["Apple", "Banana", "Mango"]

fruits.remove("Banana")

print(fruits)
```

**Output**

```
['Apple', 'Mango']
```



## pop()

Removes an element from a specific position.

If no index is given, it removes the last element.

```python
numbers = [10, 20, 30, 40]

numbers.pop(2)

print(numbers)
```

**Output**

```
[10, 20, 40]
```


## copy()

Creates a copy of a list.

```python
list1 = [1, 2, 3]

list2 = list1.copy()

print(list2)
```


## index()

Returns the position of an element.

```python
fruits = ["Apple", "Banana", "Mango"]

print(fruits.index("Banana"))
```

**Output**

```
1
```


## extend()

Adds all elements from another list.

```python
list1 = [1, 2]

list2 = [3, 4]

list1.extend(list2)

print(list1)
```

**Output**

```
[1, 2, 3, 4]
```


## reverse()

Reverses the list.

```python
numbers = [1, 2, 3]

numbers.reverse()

print(numbers)
```

**Output**

```
[3, 2, 1]
```


## sort()

Sorts the list in ascending order.

```python
numbers = [5, 2, 8, 1]

numbers.sort()

print(numbers)
```

**Output**

```
[1, 2, 5, 8]
```

Descending order

```python
numbers.sort(reverse=True)
```


## clear()

Removes all elements from the list.

```python
numbers = [1, 2, 3]

numbers.clear()

print(numbers)
```

**Output**

```
[]
```


# List Comprehension

List comprehension is a shorter and cleaner way to create a new list.

### Syntax

```python
[expression for item in iterable]
```


## Example 1

Create a list of numbers.

```python
numbers = [x for x in range(5)]

print(numbers)
```

**Output**

```
[0, 1, 2, 3, 4]
```

## Example 2

Store the squares of numbers.

```python
squares = [x * x for x in range(1, 6)]

print(squares)
```

**Output**

```
[1, 4, 9, 16, 25]
```

## Example 3

Store only even numbers.

```python
even = [x for x in range(1, 11) if x % 2 == 0]

print(even)
```

**Output**

```
[2, 4, 6, 8, 10]
```

# Things to Remember

- Lists are used to store multiple values.
- Lists are **mutable**, so they can be modified.
- Lists allow duplicate values.
- Indexing starts from **0**.
- Slicing is used to get a part of a list.
- `append()` adds an element at the end.
- `insert()` adds an element at a specific position.
- `remove()` removes an element by value.
- `pop()` removes an element by index.
- `sort()` arranges elements in ascending order.
- `reverse()` changes the order of elements.
- `clear()` removes everything from the list.
- List comprehension is a short and readable way to create new lists.


# Quick Summary

| Method | Purpose |
|---------|---------|
| `len()` | Returns the number of elements |
| `count()` | Counts the occurrence of an element |
| `append()` | Adds an element at the end |
| `insert()` | Adds an element at a specific position |
| `remove()` | Removes an element by value |
| `pop()` | Removes an element by index |
| `copy()` | Creates a copy of the list |
| `index()` | Returns the index of an element |
| `extend()` | Adds another list to the current list |
| `reverse()` | Reverses the list |
| `sort()` | Sorts the list |
| `clear()` | Removes all elements |
| List Comprehension | Creates a list in a shorter way |