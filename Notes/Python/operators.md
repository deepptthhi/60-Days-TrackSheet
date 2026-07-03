# Operators

**Operators** are symbols that perform operations on variables and values.

The values or variables on which an operator works are called **operands**.

The action performed by an operator on operand is called an **operation**.

Example:

```python
x = 10
y = 5

print(x + y)
```

In this example:

- `+` → Operator
- `10` and `5` (or `x` and `y`) → Operands

Python has different types of operators.


## 1. Arithmetic Operators

Used to perform mathematical calculations.

| Operator | Meaning | Example |
|----------|---------|---------|
| `+` | Addition | `5 + 2` |
| `-` | Subtraction | `5 - 2` |
| `*` | Multiplication | `5 * 2` |
| `/` | Division | `5 / 2` |
| `%` | Modulus (Remainder) | `5 % 2` |
| `**` | Exponent (Power) | `5 ** 2` |
| `//` | Floor Division | `5 // 2` |

Example:

```python
x = 10
y = 3

print(x + y)
print(x - y)
print(x * y)
print(x / y)
print(x % y)
print(x ** y)
print(x // y)
```

> **Remember**
>
> - `/` returns a decimal value.
> - `//` returns only the whole number.


## 2. Assignment Operators

Used to assign or update values.

| Operator | Example | Meaning |
|----------|---------|---------|
| `=` | `x = 5` | Assign value |
| `+=` | `x += 2` | `x = x + 2` |
| `-=` | `x -= 2` | `x = x - 2` |
| `*=` | `x *= 2` | `x = x * 2` |
| `/=` | `x /= 2` | `x = x / 2` |


## 3. Comparison Operators

Used to compare two values.

They always return **True** or **False**.

| Operator | Meaning |
|----------|---------|
| `==` | Equal to |
| `!=` | Not equal to |
| `>` | Greater than |
| `<` | Less than |
| `>=` | Greater than or equal to |
| `<=` | Less than or equal to |

Example:

```python
x = 10
y = 5

print(x > y)
print(x == y)
```


## 4. Logical Operators

Used to combine multiple conditions.

| Operator | Meaning |
|----------|---------|
| `and` | True if both conditions are true |
| `or` | True if at least one condition is true |
| `not` | Reverses the result |

Example:

```python
x = 5

print(x > 2 and x < 10)
print(x < 2 or x > 3)
print(not(x > 2))
```


## 5. Identity Operators

Used to check whether two variables refer to the same object.

| Operator | Meaning |
|----------|---------|
| `is` | Same object |
| `is not` | Different objects |

Example:

```python
x = [1, 2]
y = x

print(x is y)
```

> **Remember**
>
> - `==` compares **values**.
> - `is` compares **memory (object)**.


## 6. Membership Operators

Used to check if a value exists in a list, string, tuple, etc.

| Operator | Meaning |
|----------|---------|
| `in` | Value exists |
| `not in` | Value does not exist |

Example:

```python
fruits = ["Apple", "Banana", "Mango"]

print("Banana" in fruits)
print("Orange" not in fruits)
```

## 7. Bitwise Operators

Used to perform operations on binary numbers.

| Operator | Meaning |
|----------|---------|
| `&` | AND |
| `|` | OR |
| `^` | XOR |
| `~` | NOT |
| `<<` | Left Shift |
| `>>` | Right Shift |

### 1. Bitwise AND (`&`)

Returns **1** only if **both bits are 1**.

#### Truth Table

| A | B | A & B |
|---|---|:-----:|
| 0 | 0 |   0   |
| 0 | 1 |   0   |
| 1 | 0 |   0   |
| 1 | 1 |   1   |

#### Example

```python
print(6 & 3)
```

```
0110
0011
----
0010
```

**Output**

```
2
```

### 2. Bitwise OR (`|`)

Returns **1** if **at least one bit is 1**.

#### Truth Table

| A | B | A \| B |
|---|---|:------:|
| 0 | 0 |   0    |
| 0 | 1 |   1    |
| 1 | 0 |   1    |
| 1 | 1 |   1    |

#### Example

```python
print(6 | 3)
```

```
0110
0011
----
0111
```

**Output**

```
7
```

### 3. Bitwise XOR (`^`)

Returns **1** only if the bits are **different**.

#### Truth Table

| A | B | A ^ B |
|---|---|:-----:|
| 0 | 0 |   0   |
| 0 | 1 |   1   |
| 1 | 0 |   1   |
| 1 | 1 |   0   |

#### Example

```python
print(6 ^ 3)
```

```
0110
0011
----
0101
```

**Output**

```
5
```


### 4. Bitwise NOT (`~`)

Flips every bit (0 becomes 1 and 1 becomes 0).

```python
print(~6)
```

**Output**

```
-7
```

> **Note:** In Python, `~x` is equal to `-(x + 1)`.


### 5. Left Shift (`<<`)

Shifts all bits to the **left**.

```python
print(6 << 1)
```

```
0110  →  1100
```

**Output**

```
12
```

### 6. Right Shift (`>>`)

Shifts all bits to the **right**.

```python
print(6 >> 1)
```

```
0110  →  0011
```

**Output**

```
3
```

### Easy Way to Remember

| Operator | Meaning |
|----------|---------|
| `&` | Both bits must be **1** |
| `\|` | At least one bit is **1** |
| `^` | Bits must be **different** |
| `~` | Flip all bits |
| `<<` | Shift bits to the left |
| `>>` | Shift bits to the right |

> **Note:** Bitwise operators are mainly used in low-level programming, networking, embedded systems, and optimization. As a beginner, it's enough to understand the basics. Bitwise operators are an advanced topic. You don't need them for basic Python.


## 8. Walrus Operator (`:=`)

The **walrus operator** lets you assign a value to a variable while using it in an expression.

```python
numbers = [1, 2, 3, 4, 5]

if (count := len(numbers)) > 3:
    print(count)
```

> **Note:** Mostly used to make code shorter. As a beginner, you won't use it very often.


## 9. Ternary Operator

The **ternary operator** is a short way of writing an `if-else` statement.

```python
age = 20

result = "Adult" if age >= 18 else "Minor"

print(result)
```

Instead of writing:

```python
if age >= 18:
    result = "Adult"
else:
    result = "Minor"
```


## Operator Precedence

Operator precedence decides **which operation Python performs first** when there are multiple operators in the same expression.

For example:

```python
print(10 + 5 * 2)
```

**Output**

```
20
```

Python first calculates `5 * 2`, then adds `10`.

If you want addition to happen first, use parentheses.

```python
print((10 + 5) * 2)
```

**Output**

```
30
```

> **Why is it important?**
>
> Operator precedence helps Python evaluate expressions correctly without confusion. Knowing the order of operations helps you avoid mistakes while solving coding problems.


### Easy Way to Remember the operators

- **Arithmetic** → Math
- **Assignment** → Assign or update values
- **Comparison** → Compare values (`True` or `False`)
- **Logical** → Combine conditions
- **Identity** → Check if two variables are the same object
- **Membership** → Check if a value exists
- **Bitwise** → Works with binary numbers

### Easy Order to Remember the Operator precedence

1. `()` → Parentheses
2. `**` → Exponent
3. `*`, `/`, `//`, `%`
4. `+`, `-`
5. Comparison (`==`, `>`, `<`, `>=`, `<=`)
6. `not`
7. `and`
8. `or`

> **Tip:** When an expression looks confusing, use **parentheses `()`** to make the order clear and improve readability.