

## What is RegEx?

RegEx stands for **Regular Expression**.

When I first heard the name, it sounded complicated, but the basic idea is actually simple. A regular expression is just a pattern that helps us search for, match, or replace text inside a string.

Instead of checking every character manually, we can write a pattern and let Python find what we're looking for.

## Why Do We Use RegEx?

RegEx is useful when we want to:

* Search for a word or pattern in a string.
* Check if a pattern exists.
* Find all matching values.
* Replace one word with another.
* Split a string based on a pattern.

## Importing the `re` Module

Before using regular expressions, we need to import Python's built-in `re` module.

### Syntax

```python
import re
```

## `search()`

The `search()` function looks for the **first match** anywhere in the string.

If it finds the pattern, it returns a match object. Otherwise, it returns `None`.

### Syntax

```python
re.search(pattern, string)
```

### Example

```python
import re

text = "I am learning Python"

result = re.search("Python", text)

print(result)
```

**Output**

```text
<re.Match object>
```

Since the word **Python** is present, a match is found.

## `match()`

The `match()` function checks only the **beginning** of a string.

If the pattern isn't at the beginning, it returns `None`.

### Syntax

```python
re.match(pattern, string)
```

### Example

```python
import re

text = "Python is easy"

print(re.match("Python", text))
```

**Output**

```text
<re.Match object>
```

Now try this:

```python
print(re.match("easy", text))
```

**Output**

```text
None
```

This happens because `"easy"` is not at the beginning of the string.

## `findall()`

The `findall()` function returns **all the matches** as a list.

### Syntax

```python
re.findall(pattern, string)
```

### Example

```python
import re

text = "cat bat mat"

print(re.findall("at", text))
```

**Output**

```text
['at', 'at', 'at']
```

Every occurrence of `"at"` is returned.

## `split()`

The `split()` function breaks a string wherever the given pattern is found.

### Syntax

```python
re.split(pattern, string)
```

### Example

```python
import re

text = "apple,banana,grapes"

print(re.split(",", text))
```

**Output**

```text
['apple', 'banana', 'grapes']
```

The string is split wherever a comma appears.

## `sub()`

The `sub()` function replaces one pattern with another.

### Syntax

```python
re.sub(pattern, replacement, string)
```

### Example

```python
import re

text = "I like Java"

print(re.sub("Java", "Python", text))
```

**Output**

```text
I like Python
```

Here, the word **Java** is replaced with **Python**.

## Some Common RegEx Patterns

These are a few patterns that are useful to remember.

| Pattern | Meaning                                      |
| ------- | -------------------------------------------- |
| `.`     | Any single character                         |
| `\d`    | Any digit (0–9)                              |
| `\D`    | Any non-digit                                |
| `\w`    | Letter, digit or underscore                  |
| `\W`    | Any character except letters, digits and `_` |
| `\s`    | Whitespace                                   |
| `\S`    | Non-whitespace                               |
| `^`     | Beginning of a string                        |
| `$`     | End of a string                              |

### Example

```python
import re

text = "Python123"

print(re.findall(r"\d", text))
```

**Output**

```text
['1', '2', '3']
```

The pattern `\d` finds every digit in the string.

## Common Mistakes

### Forgetting to Import the Module

```python
re.search("Python", text)
```

This gives an error because the `re` module hasn't been imported.

The correct way is:

```python
import re

re.search("Python", text)
```

### Confusing `search()` and `match()`

This was a little confusing when I first learned RegEx.

The easiest way I remember it is:

* `search()` looks **anywhere** in the string.
* `match()` checks **only the beginning** of the string.

After trying a few examples, the difference became much easier to understand.

## Quick Revision

| Concept     | Description                            |
| ----------- | -------------------------------------- |
| RegEx       | A pattern used to search or match text |
| `import re` | Imports the regular expression module  |
| `search()`  | Searches anywhere in the string        |
| `match()`   | Checks only the beginning              |
| `findall()` | Returns all matches                    |
| `split()`   | Splits a string                        |
| `sub()`     | Replaces matching text                 |

## Key Takeaways

* RegEx is used to search, match, and replace text using patterns.
* Python provides the built-in `re` module for working with regular expressions.
* `search()` looks for a match anywhere in the string.
* `match()` checks only the beginning of the string.
* `findall()` returns every match as a list.
* `split()` breaks a string based on a pattern.
* `sub()` replaces one pattern with another.
* Learning a few common patterns like `\d`, `\w`, and `\s` is enough to get started with RegEx.
