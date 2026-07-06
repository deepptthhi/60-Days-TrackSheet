

## What are Booleans?

## Why Do We Use Booleans?

## Boolean Values
- True
- False

## The bool() Function
- Syntax
- Example
- Output

## Truthy Values
- Explanation
- Examples

## Falsy Values
- Explanation
- Examples

## Booleans in Conditional Statements
(Simple note saying Booleans are commonly used with if statements.)

### Example

```python
age = 20

if age >= 18:
    print("Eligible to vote")
```

Output

```
Eligible to vote
```

## Common Mistakes

### Empty values are False

```python
print(bool([]))
print(bool(""))
print(bool(0))
```

### Confusing True/False with strings

```python
print(bool("False"))
print(bool(False))
```

Output

```
True
False
```

## Quick Revision

| Concept | Description |
|----------|-------------|
| Boolean | True or False |
| bool() | Converts a value to True or False |
| Truthy | Values treated as True |
| Falsy | Values treated as False |

## Key Takeaways

- A Boolean has only two values: `True` and `False`.
- `bool()` converts values into Boolean values.
- Non-empty values are usually `True`.
- Empty values and `0` are usually `False`.
- Booleans are commonly used in decision-making statements like `if`.