

## What is a String?

A string is simply **text** stored in a variable.

It can contain letters, numbers, spaces, or symbols. In Python, strings are written inside single quotes (`' '`), double quotes (`" "`), or triple quotes (`""" """` or `''' '''`).

```python
name = "Deepthi"
city = 'Bengaluru'
message = """Welcome to Python"""
```

> **Note:** Strings are immutable, which means once a string is created, its characters cannot be changed directly.


## Creating a String

There are different ways to create a string.

```python
text1 = "Python"
text2 = 'Programming'
text3 = """This is a
multiline string."""
```


## String Indexing

Every character in a string has its own position, called an **index**.

Indexing starts from **0**.

```python
text = "Python"
```

| Character | P | y | t | h | o | n |
|-----------|---|---|---|---|---|---|
| Index | 0 | 1 | 2 | 3 | 4 | 5 |
| Negative Index | -6 | -5 | -4 | -3 | -2 | -1 |

```python
print(text[0])
print(text[-1])
```

**Output**

```
P
n
```


## String Slicing

Slicing lets us take only the part of the string that we need.

### Syntax

```python
string[start:end]
```

The **start index is included**, but the **end index is not**.

```python
text = "Python"

print(text[0:2])
print(text[2:6])
print(text[:4])
print(text[3:])
print(text[::-1])
```

**Output**

```
Py
thon
Pyth
hon
nohtyP
```


# Common String Methods

## len()

Returns the total number of characters in a string.

```python
text = "Python"

print(len(text))
```


## count()

Counts how many times a character or word appears.

```python
text = "banana"

print(text.count("a"))
```


## upper()

Converts every letter to uppercase.

```python
text = "python"

print(text.upper())
```



## lower()

Converts every letter to lowercase.

```python
text = "PYTHON"

print(text.lower())
```



## capitalize()

Makes only the first letter uppercase.

```python
text = "python"

print(text.capitalize())
```



## title()

Makes the first letter of every word uppercase.

```python
text = "hello world"

print(text.title())
```



## index()

Returns the position of the first occurrence.

If the value is not found, Python gives an error.

```python
text = "Python"

print(text.index("t"))
```



## find()

Works like `index()`, but instead of giving an error, it returns **-1** if the value is not found.

```python
text = "Python"

print(text.find("o"))
```



## rindex()

Returns the last occurrence of a character.

```python
text = "banana"

print(text.rindex("a"))
```



## rfind()

Returns the last occurrence of a character.

Returns **-1** if the value is not found.

```python
text = "banana"

print(text.rfind("a"))
```



## replace()

Replaces one part of the string with another.

```python
text = "I like Java"

print(text.replace("Java", "Python"))
```



## format()

Inserts values into a string.

```python
name = "Deepthi"

print("Hello {}".format(name))
```



## center()

Places the string in the center.

```python
text = "Python"

print(text.center(12))
```



## casefold()

Converts the string to lowercase.

It is mainly used when comparing two strings without worrying about uppercase or lowercase letters.

```python
text = "PYTHON"

print(text.casefold())
```


# String Checking Methods

These methods always return either **True** or **False**.

### isalnum()

Checks whether the string contains only letters and numbers.

```python
"Python123".isalnum()
```

### isalpha()

Checks whether all characters are letters.

```python
"Python".isalpha()
```

### isdecimal()

Checks whether all characters are decimal numbers.

```python
"123".isdecimal()
```

### isdigit()

Checks whether all characters are digits.

```python
"123".isdigit()
```

### isnumeric()

Checks whether all characters are numeric.

```python
"123".isnumeric()
```

### islower()

Checks if all letters are lowercase.

```python
"python".islower()
```

### isupper()

Checks if all letters are uppercase.

```python
"PYTHON".isupper()
```

### isspace()

Checks whether the string contains only spaces.

```python
"   ".isspace()
```


# More Useful Methods

### startswith()

Checks whether the string starts with a given value.

```python
"Python".startswith("Py")
```

### endswith()

Checks whether the string ends with a given value.

```python
"Python".endswith("on")
```

### swapcase()

Changes uppercase letters to lowercase and lowercase letters to uppercase.

```python
"PyThOn".swapcase()
```

### strip()

Removes extra spaces from both ends of a string.

```python
"  Hello  ".strip()
```

### ljust()

Aligns the text to the left.

```python
"Python".ljust(10, "-")
```

### rjust()

Aligns the text to the right.

```python
"Python".rjust(10, "-")
```


# String Concatenation

Concatenation simply means joining two or more strings.

```python
first = "Hello"
second = "World"

print(first + " " + second)
```

**Output**

```
Hello World
```

# Easy to remember

- Strings are used to store text.
- Strings are immutable, so they cannot be changed directly.
- Indexing gives one character.
- Slicing gives part of a string.
- `find()` returns **-1** if the value is not found, while `index()` gives an error.
- `rfind()` and `rindex()` work from the right side.
- `strip()` removes unwanted spaces.
- `replace()` changes one value to another.
- `startswith()` and `endswith()` are useful for checking prefixes and suffixes.
- Use `+` to join strings.