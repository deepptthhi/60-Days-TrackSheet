# Arrays

## What are Arrays?

An array is one of the simplest data structures. 

It stores a group of values of the **same data type** in continuous memory locations.

Think of it like a row of lockers. Every locker has a number (index), so if you know the index, you can directly reach that element without checking the others.

Example:

```
Index : 0   1   2   3   4
Array : 10  20  30  40  50
```

## Things to Remember

- Stores only one type of data.
- Elements are stored next to each other in memory.
- Index starts from **0**.
- Size is usually fixed after creation.
- Accessing an element is very fast because we already know its index.

## Common Operations

| Operation | What it does | Time |
|-----------|--------------|------|
| Access | Get an element using its index | O(1) |
| Search | Find an element | O(n) |
| Insert | Add an element | O(n) |
| Delete | Remove an element | O(n) |
| Update | Change an element | O(1) |


## Advantages

- Fast access to elements.
- Easy to understand and implement.
- Uses memory efficiently.


## Disadvantages

- Size cannot be changed easily.
- Insertion and deletion are expensive because elements may need to be shifted.


## Where are Arrays used?

- Storing marks, IDs, salaries, etc.
- Matrices
- Image processing
- Building other data structures like stacks and heaps

## Quick Summary

- Same data type
- Continuous memory
- Fast access
- Fixed size
- Slow insertion and deletion