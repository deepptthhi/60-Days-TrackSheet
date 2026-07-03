# Linked Lists

## What is a Linked List?

A linked list is a linear data structure made up of **nodes**. 

Each node stores two things:

- The actual data
- The address (pointer) of the next node

Unlike arrays, the nodes are **not stored next to each other in memory**. Instead, each node points to the next one.

Example:

```
10 → 20 → 30 → 40 → NULL
```

## Things to Remember

- Nodes can be stored anywhere in memory.
- Every node knows where the next node is.
- The size can grow or shrink whenever needed.
- We cannot directly jump to an element like in an array.
- To reach a node, we have to start from the beginning.

## Common Operations

| Operation | What it does | Time |
|-----------|--------------|------|
| Traverse | Visit every node | O(n) |
| Search | Find a node | O(n) |
| Insert (Beginning) | Add a new node at the start | O(1) |
| Delete (Beginning) | Remove the first node | O(1) |

## Advantages

- Size is dynamic.
- Insertion and deletion are fast.
- No need for continuous memory.

## Disadvantages

- Cannot access elements directly.
- Uses extra memory to store pointers.
- Searching is slower than arrays.

## Where are Linked Lists used?

- Browser history
- Music playlists
- Implementing stacks and queues
- Memory management


## Quick Summary

- Made of nodes
- Uses pointers
- Dynamic size
- Fast insertion and deletion
- Slow searching