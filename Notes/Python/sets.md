

## What is a Set?

A set is a built-in data structure used to store **unique values**. Unlike lists, a set automatically removes duplicate values. Sets are mainly used when we only care about unique data and don't need indexing.

### Key Points

* Stores only unique values.
* Duplicate values are removed automatically.
* Sets are mutable, so we can add or remove elements.
* Sets are unordered, so the output order may change.
* Sets do not support indexing or slicing.

## Creating a Set

A set can be created using curly braces `{}` or the `set()` function.

### Syntax

```python
set_name = {value1, value2, value3}
```

### Example

```python
numbers = {1, 2, 3, 4}

print(numbers)
```

**Output**

```text
{1, 2, 3, 4}
```

## Creating an Empty Set

An empty set cannot be created using `{}` because it creates an empty dictionary.

### Syntax

```python
set_name = set()
```

### Example

```python
numbers = set()

print(numbers)
```

**Output**

```text
set()
```

## Features of a Set

### Unique Values

A set automatically removes duplicate values.

### Example

```python
numbers = {1, 2, 2, 3, 4, 4, 5}

print(numbers)
```

**Output**

```text
{1, 2, 3, 4, 5}
```

Even though `2` and `4` were added twice, they appear only once.

---

### Unordered

A set does not maintain the order of elements.

```python
colors = {"red", "blue", "green"}

print(colors)
```

**Output**

```text
{'green', 'red', 'blue'}
```

> The order may be different every time you run the program.

---

### Mutable

We can add or remove elements after creating the set.

```python
numbers = {1, 2, 3}

numbers.add(4)

print(numbers)
```

**Output**

```text
{1, 2, 3, 4}
```

---

### No Indexing

Sets don't support indexing.

```python
numbers = {10, 20, 30}

print(numbers[0])
```

**Output**

```text
TypeError
```

If you need indexing, use a list instead.

## Adding Elements

### `add()`

`add()` is used to insert a single element into a set.

### Syntax

```python
set_name.add(value)
```

### Example

```python
numbers = {1, 2, 3}

numbers.add(4)

print(numbers)
```

**Output**

```text
{1, 2, 3, 4}
```

---

### `update()`

`update()` is used to add multiple elements at once.

### Syntax

```python
set_name.update(iterable)
```

### Example

```python
numbers = {1, 2, 3}

numbers.update([4, 5, 6])

print(numbers)
```

**Output**

```text
{1, 2, 3, 4, 5, 6}
```

## Removing Elements

### `remove()`

`remove()` deletes the specified element.

If the element is not found, Python raises an error.

### Syntax

```python
set_name.remove(value)
```

### Example

```python
numbers = {1, 2, 3, 4}

numbers.remove(2)

print(numbers)
```

**Output**

```text
{1, 3, 4}
```

---

### `discard()`

`discard()` also removes an element, but it doesn't raise an error if the element is missing.

### Syntax

```python
set_name.discard(value)
```

### Example

```python
numbers = {1, 2, 3}

numbers.discard(5)

print(numbers)
```

**Output**

```text
{1, 2, 3}
```

---

### `pop()`

`pop()` removes and returns a random element because sets are unordered.

### Syntax

```python
set_name.pop()
```

### Example

```python
numbers = {10, 20, 30}

numbers.pop()

print(numbers)
```

**Output**

```text
Output may vary because sets are unordered.
```

---

### `clear()`

`clear()` removes every element from the set.

### Syntax

```python
set_name.clear()
```

### Example

```python
numbers = {1, 2, 3}

numbers.clear()

print(numbers)
```

**Output**

```text
set()
```

## Looping Through a Set

We can use a `for` loop to access each element.

### Syntax

```python
for item in set_name:
    print(item)
```

### Example

```python
fruits = {"Apple", "Banana", "Mango"}

for fruit in fruits:
    print(fruit)
```

**Output**

```text
Apple
Banana
Mango
```

> The order may be different because sets are unordered.

## Checking Membership

Membership operators are useful to check whether an element exists in a set.

### Using `in`

```python
numbers = {1, 2, 3, 4}

print(3 in numbers)
```

**Output**

```text
True
```

---

### Using `not in`

```python
numbers = {1, 2, 3, 4}

print(5 not in numbers)
```

**Output**

```text
True
```

## Set Operations

One of the biggest advantages of sets is that they make operations like finding common or unique values very easy.

### `union()`

Returns all unique elements from both sets.

### Syntax

```python
set1.union(set2)
```

### Example

```python
A = {1, 2, 3}
B = {3, 4, 5}

print(A.union(B))
```

**Output**

```text
{1, 2, 3, 4, 5}
```

---

### `intersection()`

Returns only the common elements.

### Syntax

```python
set1.intersection(set2)
```

### Example

```python
A = {1, 2, 3}
B = {2, 3, 4}

print(A.intersection(B))
```

**Output**

```text
{2, 3}
```

---

### `difference()`

Returns the elements that are present in the first set but not in the second.

### Syntax

```python
set1.difference(set2)
```

### Example

```python
A = {1, 2, 3}
B = {2, 3, 4}

print(A.difference(B))
```

**Output**

```text
{1}
```

---

### `symmetric_difference()`

Returns the elements that are present in either set but not in both.

### Syntax

```python
set1.symmetric_difference(set2)
```

### Example

```python
A = {1, 2, 3}
B = {2, 3, 4}

print(A.symmetric_difference(B))
```

**Output**

```text
{1, 4}
```
# Set Methods

Python provides many built-in methods to make working with sets easier. These methods help us add, remove, copy, compare, and combine sets.

## `copy()`

`copy()` creates another set with the same elements. This is useful when you want to keep the original set unchanged.

### Syntax

```python
new_set = set_name.copy()
```

### Example

```python
numbers = {1, 2, 3}

new_numbers = numbers.copy()

print(new_numbers)
```

**Output**

```text
{1, 2, 3}
```


## `issubset()`

`issubset()` checks whether all the elements of one set are present in another set.

### Syntax

```python
set1.issubset(set2)
```

### Example

```python
A = {1, 2}
B = {1, 2, 3, 4}

print(A.issubset(B))
```

**Output**

```text
True
```


## `issuperset()`

`issuperset()` checks whether one set contains all the elements of another set.

### Syntax

```python
set1.issuperset(set2)
```

### Example

```python
A = {1, 2, 3, 4}
B = {1, 2}

print(A.issuperset(B))
```

**Output**

```text
True
```

## `isdisjoint()`

`isdisjoint()` checks whether two sets have no common elements.

### Syntax

```python
set1.isdisjoint(set2)
```

### Example

```python
A = {1, 2}
B = {3, 4}

print(A.isdisjoint(B))
```

**Output**

```text
True
```

If the sets have at least one common element, it returns `False`.


# Frozen Set

## What is a Frozen Set?

A **frozenset** is an immutable version of a set. Once it is created, you cannot add or remove elements.

It is useful when the data should not be modified.

### Syntax

```python
frozenset(iterable)
```

### Example

```python
numbers = frozenset([1, 2, 3, 4])

print(numbers)
```

**Output**

```text
frozenset({1, 2, 3, 4})
```

Trying to add an element gives an error.

```python
numbers.add(5)
```

**Output**

```text
AttributeError
```



# Quick Revision

| Operation               | Method                   |
| ----------------------- | ------------------------ |
| Create a set            | `{}` or `set()`          |
| Create an empty set     | `set()`                  |
| Add one element         | `add()`                  |
| Add multiple elements   | `update()`               |
| Remove an element       | `remove()`               |
| Remove safely           | `discard()`              |
| Remove a random element | `pop()`                  |
| Remove everything       | `clear()`                |
| Copy a set              | `copy()`                 |
| Check membership        | `in`, `not in`           |
| Combine two sets        | `union()`                |
| Find common elements    | `intersection()`         |
| Find different elements | `difference()`           |
| Find uncommon elements  | `symmetric_difference()` |
| Check subset            | `issubset()`             |
| Check superset          | `issuperset()`           |
| Check disjoint sets     | `isdisjoint()`           |
| Immutable set           | `frozenset()`            |



# Common Mistakes

## 1. Duplicate Values

```python
numbers = {1, 2, 2, 3, 3}

print(numbers)
```

**Output**

```text
{1, 2, 3}
```

Duplicate values are removed automatically.



## 2. Using Indexing

```python
numbers = {10, 20, 30}

print(numbers[0])
```

**Output**

```text
TypeError
```

Sets don't support indexing.



## 3. Creating an Empty Set

```python
empty = {}
```

This creates an **empty dictionary**, not a set.

To create an empty set:

```python
empty = set()
```



## 4. Using `remove()` on a Missing Element

```python
numbers = {1, 2, 3}

numbers.remove(5)
```

**Output**

```text
KeyError
```

If you're not sure whether the element exists, use `discard()` instead.


# When Should I Use a Set?

A set is a good choice when:

* You only need unique values.
* You want to remove duplicates.
* You need to compare two collections.
* You want to find common or different values quickly.
* You don't need indexing.

Some real-world examples are:

* Removing duplicate names from a list.
* Finding common subjects between two students.
* Comparing skills of two candidates.
* Finding unique visitors on a website.



# Key Takeaways

* A set stores only **unique values**.
* Duplicate values are removed automatically.
* Sets are unordered.
* Sets don't support indexing.
* `add()` adds one element.
* `update()` adds multiple elements.
* `remove()` deletes an element but raises an error if it doesn't exist.
* `discard()` removes an element safely.
* `pop()` removes a random element.
* `union()` combines two sets.
* `intersection()` finds common elements.
* `difference()` finds elements present only in the first set.
* `symmetric_difference()` finds elements that are unique to each set.
* `frozenset()` creates a read-only set.



# Interview Tip

A common interview question is:

**List vs Set**

| List                    | Set                          |
| ----------------------- | ---------------------------- |
| Allows duplicate values | Stores only unique values    |
| Ordered                 | Unordered                    |
| Supports indexing       | No indexing                  |
| Uses `[]`               | Uses `{}` or `set()`         |
| Best when order matters | Best when uniqueness matters |

> **Remember:** If you need to remove duplicates or perform operations like union and intersection, a **set** is usually the better choice. If you need indexing or want to preserve order, use a **list**.
