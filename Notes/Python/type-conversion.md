# Type Conversion (Type Casting)

Sometimes we need to change one data type into another. This is called **type conversion** or **type casting**.

For example:

- `"25"` → `25`
- `10` → `10.0`

>  Type Conversion → The general process of changing one data type to another. Automatic (Implicit)
>  Type Casting  → Usually refers to explicit (manual) conversion done by the programmer.

Python can do this in two ways.


## 1. Implicit Type Conversion

In **implicit conversion**, Python automatically converts the data type when needed.

```python
x = 10
y = 2.5

result = x + y

print(result)
print(type(result))
```

**Output**

```
12.5
<class 'float'>
```

> Here, Python automatically converts `10` (`int`) into `10.0` (`float`) before adding.


## 2. Explicit Type Conversion (Type Casting)

In **explicit conversion**, we manually change the data type using built-in functions.

### String → Integer

```python
age = "21"
age = int(age)

print(age)
```

### Integer → Float

```python
num = 10
num = float(num)

print(num)
```

### Number → String

```python
num = 100
text = str(num)

print(text)
```

### Number → Boolean

```python
print(bool(1))
print(bool(0))
```

**Output**

```
True
False
```


## Common Conversion Functions

| Function | Converts To |
|----------|-------------|
| `int()` | Integer |
| `float()` | Float |
| `str()` | String |
| `bool()` | Boolean |


## Easy Way to Remember

- **Implicit Conversion** → Python does it automatically.
- **Explicit Conversion (Type Casting)** → You do it manually using functions like `int()`, `float()`, `str()`, or `bool()`.