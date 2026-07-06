

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
# String Formatting

## What is String Formatting?

String formatting is a way of inserting values into a string.

Instead of joining strings and variables using the `+` operator, Python gives us easier and cleaner ways to display values inside a string.

## Why Do We Use String Formatting?

String formatting helps us:

* Display variables inside a string.
* Make the output easier to read.
* Write cleaner code.
* Create dynamic messages.

## Method 1: f-Strings (Recommended)

An f-string is the easiest and most commonly used way to format strings.

We simply add `f` before the string and place variables inside curly braces `{}`.

### Syntax

```python
f"Text {variable}"
```

### Example

```python
name = "Deepthi"
age = 22

print(f"My name is {name} and I am {age} years old.")
```

**Output**

```
My name is Deepthi and I am 22 years old.
```

I found this method the easiest because it's simple to read and doesn't need any extra functions.

## Method 2: format()

The `format()` method is another way to insert values into a string.

### Syntax

```python
"Text {}".format(value)
```

### Example

```python
name = "Deepthi"
age = 22

print("My name is {} and I am {} years old.".format(name, age))
```

**Output**

```
My name is Deepthi and I am 22 years old.
```

The values are placed in the same order as they are passed to `format()`.

## Using Index Numbers

We can also choose which value should be placed where by using index numbers.

```python
print("{1} is learning {0}".format("Python", "Deepthi"))
```

**Output**

```
Deepthi is learning Python
```

## Using Named Values

Instead of using index numbers, we can give each value a name.

```python
print("My name is {name}".format(name="Deepthi"))
```

**Output**

```
My name is Deepthi
```

This makes the code a little easier to understand, especially when there are many values.

## Formatting Numbers

We can also control how numbers are displayed.

### Showing Decimal Places

```python
price = 99.4567

print(f"{price:.2f}")
```

**Output**

```
99.46
```

The number is displayed with only two decimal places.

### Adding Commas

```python
amount = 1000000

print(f"{amount:,}")
```

**Output**

```
1,000,000
```

This makes large numbers much easier to read.

### Showing Percentage

```python
score = 0.85

print(f"{score:.0%}")
```

**Output**

```
85%
```

## Aligning Text

Sometimes we want the output to look neat, especially when printing tables.

### Left Align

```python
name = "Python"

print(f"{name:<10}")
```

### Right Align

```python
name = "Python"

print(f"{name:>10}")
```

### Center Align

```python
name = "Python"

print(f"{name:^10}")
```

These are mostly useful when displaying reports or tabular data.

## Common Mistakes

### Forgetting the `f`

```python
name = "Deepthi"

print("Hello {name}")
```

**Output**

```
Hello {name}
```

The variable is not replaced because the string doesn't start with `f`.

Correct way:

```python
name = "Deepthi"

print(f"Hello {name}")
```

### Forgetting Curly Braces

```python
name = "Deepthi"

print(f"Hello name")
```

This prints the word **name** instead of the variable.

The correct way is:

```python
print(f"Hello {name}")
```

# Easy to Remember

- Strings are used to store text.
- Strings are immutable, so they cannot be changed directly.
- Indexing returns a single character.
- Slicing returns a part of the string.
- `find()` returns **-1** if the value is not found, while `index()` gives an error.
- `rfind()` and `rindex()` search from the right side of the string.
- `replace()` is used to replace one part of a string with another.
- `strip()` removes extra spaces from the beginning and end of a string.
- `startswith()` and `endswith()` are useful for checking prefixes and suffixes.
- Use `+` to join two or more strings.
- Use **f-strings** when you want to insert variables into a string because they are simple and easy to read.
- The `format()` method is another way to insert values into a string and is commonly seen in older Python code.
- String formatting helps make the output cleaner and easier to read.