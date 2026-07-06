# Python Datetime

## What is Datetime?

The `datetime` module helps us work with dates and time in Python.

Instead of finding the current date or time manually, Python already provides a module that can do it for us. It also lets us display dates in different formats whenever we need them.

## Why Do We Use Datetime?

The `datetime` module is useful when we want to:

* Get today's date.
* Get the current time.
* Display both date and time together.
* Show dates in different formats.
* Work with dates and time in our programs.

## Importing the Datetime Module

Before using it, we need to import the module.

### Syntax

```python
import datetime
```

## Getting the Current Date and Time

The `now()` function returns the current date and time.

### Syntax

```python
datetime.datetime.now()
```

### Example

```python
import datetime

current = datetime.datetime.now()

print(current)
```

**Output**

```text
2026-07-07 18:45:30.123456
```

The output will be different because it depends on the current date and time on your computer.

## Getting Only the Current Date

If we only need today's date, we can use `date.today()`.

### Example

```python
import datetime

today = datetime.date.today()

print(today)
```

**Output**

```text
2026-07-07
```

## Getting Only the Current Time

If we only need the time, we can use the `time()` method.

### Example

```python
import datetime

current = datetime.datetime.now()

print(current.time())
```

**Output**

```text
18:45:30.123456
```

## Creating Our Own Date

We don't always have to use the current date. We can also create a date by giving the year, month, and day.

### Syntax

```python
datetime.datetime(year, month, day)
```

### Example

```python
import datetime

birthday = datetime.datetime(2004, 5, 15)

print(birthday)
```

**Output**

```text
2004-05-15 00:00:00
```

## Formatting Dates with `strftime()`

Sometimes the default format isn't easy to read.

The `strftime()` method lets us display the date in the format we want.

### Syntax

```python
date.strftime(format)
```

### Example

```python
import datetime

current = datetime.datetime.now()

print(current.strftime("%d-%m-%Y"))
```

**Output**

```text
07-07-2026
```

Instead of the default format, the date is now displayed as **day-month-year**.

## Some Common Format Codes

These are the format codes that I'll probably use most often.

| Code | Meaning          |
| ---- | ---------------- |
| `%d` | Day              |
| `%m` | Month            |
| `%Y` | Full Year        |
| `%y` | Short Year       |
| `%B` | Full Month Name  |
| `%b` | Short Month Name |
| `%A` | Full Day Name    |
| `%a` | Short Day Name   |
| `%H` | Hour (24-hour)   |
| `%I` | Hour (12-hour)   |
| `%M` | Minutes          |
| `%S` | Seconds          |

### Example

```python
import datetime

current = datetime.datetime.now()

print(current.strftime("%A"))
print(current.strftime("%B"))
print(current.strftime("%Y"))
```

**Output**

```text
Tuesday
July
2026
```

## Common Mistakes

### Forgetting to Import the Module

```python
print(datetime.datetime.now())
```

This gives an error because Python doesn't know what `datetime` is.

The correct way is:

```python
import datetime

print(datetime.datetime.now())
```

### Confusing `date.today()` and `datetime.now()`

This confused me at first.

* `date.today()` returns **only the date**.
* `datetime.now()` returns **both the date and the current time**.

Once I tried both, the difference became much clearer.

## Quick Revision

| Concept           | Description                       |
| ----------------- | --------------------------------- |
| `import datetime` | Imports the datetime module       |
| `datetime.now()`  | Returns the current date and time |
| `date.today()`    | Returns today's date              |
| `time()`          | Returns only the current time     |
| `strftime()`      | Formats the date and time         |

## Key Takeaways

* The `datetime` module makes it easy to work with dates and time.
* `datetime.now()` gives both the current date and time.
* `date.today()` returns only today's date.
* `time()` returns only the current time.
* `strftime()` helps display dates in different formats.
* Different format codes can be combined to display dates exactly the way we want.
