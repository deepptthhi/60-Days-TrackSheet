
# Python Practice Programs — Loops & Conditional Statements

These programs use only the concepts learned so far:
- `if`, `if-else`, `if-elif`
- `for` loop
- `while` loop
- Nested loops


## 1. Check if a Number is Prime

```python
num = int(input("Enter a number: "))

if num <= 1:
    print("Not a Prime Number")
else:
    is_prime = True

    for i in range(2, num):
        if num % i == 0:
            is_prime = False
            break

    if is_prime:
        print("Prime Number")
    else:
        print("Not a Prime Number")
```

### Sample Output

```
Enter a number: 13
Prime Number
```


## 2. Print Multiplication Table

```python
num = int(input("Enter a number: "))

for i in range(1, 11):
    print(f"{num} x {i} = {num * i}")
```

### Sample Output

```
Enter a number: 5

5 x 1 = 5
5 x 2 = 10
5 x 3 = 15
...
5 x 10 = 50
```


## 3. Print a Right-Angle Triangle Pattern (Nested Loops)

```python
rows = int(input("Enter number of rows: "))

for i in range(1, rows + 1):
    for j in range(i):
        print("*", end=" ")
    print()
```

### Sample Output

```
Enter number of rows: 5

*
* *
* * *
* * * *
* * * * *
```


## 4. Sum of Digits of a Number

```python
num = int(input("Enter a number: "))

sum_digits = 0

while num > 0:
    digit = num % 10
    sum_digits += digit
    num = num // 10

print("Sum of digits =", sum_digits)
```

### Sample Output

```
Enter a number: 12345

Sum of digits = 15
```

## 5. Reverse a Number Using a Loop

```python
num = int(input("Enter a number: "))

reverse = 0

while num > 0:
    digit = num % 10
    reverse = reverse * 10 + digit
    num = num // 10

print("Reversed number =", reverse)
```

### Sample Output

```
Enter a number: 12345

Reversed number = 54321
```

## Concepts Used

| Program | Concepts Used |
|----------|---------------|
| Prime Number | `if`, `for`, `break`, modulus `%` |
| Multiplication Table | `for` loop, `range()` |
| Triangle Pattern | Nested `for` loops |
| Sum of Digits | `while` loop, `%`, `//` |
| Reverse Number | `while` loop, `%`, `//`, arithmetic operations |