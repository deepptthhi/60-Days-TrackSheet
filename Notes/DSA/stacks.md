# Stacks

## What is a Stack?

A stack is a linear data structure that follows the **LIFO (Last In, First Out)** principle.

This means the last element added is the first one to be removed.

Think of a stack of books. You always place a new book on the top and also remove the topmost book first.

Example:

```
Top
40
30
20
10
Bottom
```


## Things to Remember

- Insertion and deletion happen only at the top.
- Follows the LIFO rule.
- Very fast for adding and removing elements.


## Common Operations

| Operation | What it does | Time |
|-----------|--------------|------|
| Push | Add an element | O(1) |
| Pop | Remove the top element | O(1) |
| Peek | View the top element | O(1) |
| IsEmpty | Check whether the stack is empty | O(1) |



## Advantages

- Easy to implement.
- Push and Pop operations are very fast.
- Perfect for reversing operations.



## Disadvantages

- Only the top element can be accessed directly.
- Middle elements cannot be accessed.



## Where are Stacks used?

- Function calls (Call Stack)
- Undo and Redo
- Parentheses matching
- Expression evaluation
- Backtracking problems



## Quick Summary

- Follows LIFO
- Push and Pop happen at the top
- Fast insertion and deletion
- Used in recursion and undo operations