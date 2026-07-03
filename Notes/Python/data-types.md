# Data Types

A **data type** tells Python what kind of value a variable is storing.

Use `type()` to check the data type.

```python
x = 10
print(type(x))
```


## Text Type (`str`)

Stores text or characters.

```python
name = "Deepthi"
```


## Numeric Types

Used to store numbers.

| Data Type | Example |
|-----------|---------|
| `int` | `10` |
| `float` | `10.5` |
| `complex` | `2 + 3j` |

```python
age = 21
price = 99.99
num = 2 + 3j
```



## Sequence Types

Used to store multiple values.

| Data Type | Description |
|-----------|-------------|
| `list` | Ordered and changeable |
| `tuple` | Ordered but cannot be changed |
| `range` | Generates a sequence of numbers |

```python
fruits = ["Apple", "Banana", "Mango"]   # List

colors = ("Red", "Green", "Blue")       # Tuple

numbers = range(5)                      # Range
```


## Mapping Type (`dict`)

Stores data as **key-value pairs**.

```python
student = {
    "name": "Deepthi",
    "age": 21
}
```


## Set Types

Stores unique values.

| Data Type | Description |
|-----------|-------------|
| `set` | Unordered and unique values |
| `frozenset` | Immutable version of a set |

```python
fruits = {"Apple", "Banana", "Mango"}
```


## Boolean Type (`bool`)

Stores only two values:

- `True`
- `False`

```python
is_logged_in = True
```



## Binary Types

Used for binary (byte) data.

- `bytes`
- `bytearray`
- `memoryview`

> These are mainly used in advanced topics like file handling and networking.


## None Type (`None`)

Represents **no value** or an empty value.

```python
x = None
```

> **Remember**
> - `str` → Text
> - `int`, `float`, `complex` → Numbers
> - `list`, `tuple`, `range` → Collections
> - `dict` → Key-value pairs
> - `set` → Unique values
> - `bool` → True/False
> - `None` → No value