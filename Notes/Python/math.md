

## What is the Math Module?

The `math` module is a built-in module in Python that provides functions for mathematical calculations.

Instead of writing our own logic for common calculations, we can simply use the functions that Python already provides. This makes the code shorter and saves time.

## Why Do We Use the Math Module?

The `math` module is useful when we need to:

* Find the square root of a number.
* Calculate powers.
* Round numbers up or down.
* Find factorials.
* Use mathematical constants like π (pi).

## Importing the Math Module

Before using any function from the `math` module, we need to import it.

### Syntax

```python
import math
```

## Square Root – `sqrt()`

The `sqrt()` function returns the square root of a number.

### Syntax

```python
math.sqrt(number)
```

### Example

```python
import math

print(math.sqrt(25))
```

**Output**

```text
5.0
```

This returns the square root of `25`, which is `5`.

## Power – `pow()`

The `pow()` function raises a number to a given power.

### Syntax

```python
math.pow(base, exponent)
```

### Example

```python
import math

print(math.pow(2, 3))
```

**Output**

```text
8.0
```

Here, `2` is raised to the power of `3`.

## Ceiling – `ceil()`

The `ceil()` function always rounds a number **up** to the next whole number.

### Syntax

```python
math.ceil(number)
```

### Example

```python
import math

print(math.ceil(4.2))
```

**Output**

```text
5
```

Even though the decimal part is small, the number is rounded up.

## Floor – `floor()`

The `floor()` function always rounds a number **down** to the nearest whole number.

### Syntax

```python
math.floor(number)
```

### Example

```python
import math

print(math.floor(4.9))
```

**Output**

```text
4
```

No matter what the decimal part is, the number is rounded down.

## Factorial – `factorial()`

The `factorial()` function returns the factorial of a number.

A factorial is the product of all positive numbers from `1` up to that number.

For example,

`5! = 5 × 4 × 3 × 2 × 1 = 120`

### Syntax

```python
math.factorial(number)
```

### Example

```python
import math

print(math.factorial(5))
```

**Output**

```text
120
```

## Pi – `pi`

The `pi` constant gives the value of π.

It is commonly used in mathematical calculations involving circles.

### Syntax

```python
math.pi
```

### Example

```python
import math

print(math.pi)
```

**Output**

```text
3.141592653589793
```

## Euler's Number – `e`

The `e` constant returns the value of Euler's number.

It is mainly used in advanced mathematical calculations.

### Syntax

```python
math.e
```

### Example

```python
import math

print(math.e)
```

**Output**

```text
2.718281828459045
```

## Absolute Value – `abs()`

The `abs()` function returns the positive value of a number.

Unlike the previous functions, `abs()` is a built-in function, so we don't need to import the `math` module.

### Syntax

```python
abs(number)
```

### Example

```python
print(abs(-15))
```

**Output**

```text
15
```

## Round – `round()`

The `round()` function rounds a number to the nearest whole number.

This is also a built-in function.

### Syntax

```python
round(number)
```

### Example

```python
print(round(8.6))
print(round(8.3))
```

**Output**

```text
9
8
```

## Common Mistakes

### Forgetting to Import the Module

```python
print(math.sqrt(16))
```

This gives an error because the `math` module hasn't been imported.

The correct way is:

```python
import math

print(math.sqrt(16))
```

### Confusing `ceil()` and `floor()`

This confused me at first because both are used for rounding.

The easiest way to remember them is:

* `ceil()` always rounds **up**.
* `floor()` always rounds **down**.

After trying a few examples, the difference became much easier to understand.

## Quick Revision

| Concept            | Description                            |
| ------------------ | -------------------------------------- |
| `math.sqrt()`      | Finds the square root of a number      |
| `math.pow()`       | Raises a number to a power             |
| `math.ceil()`      | Always rounds up                       |
| `math.floor()`     | Always rounds down                     |
| `math.factorial()` | Finds the factorial of a number        |
| `math.pi`          | Returns the value of π                 |
| `math.e`           | Returns Euler's number                 |
| `abs()`            | Returns the positive value of a number |
| `round()`          | Rounds to the nearest whole number     |

## Key Takeaways

* The `math` module provides ready-to-use mathematical functions.
* Import the module before using its functions.
* `sqrt()` is used to find the square root.
* `pow()` calculates powers.
* `ceil()` and `floor()` round numbers differently.
* `factorial()` finds the factorial of a number.
* `pi` and `e` are built-in mathematical constants.
* `abs()` and `round()` are built-in functions, so they don't need the `math` module.
