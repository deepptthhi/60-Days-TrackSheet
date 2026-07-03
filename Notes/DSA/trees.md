# Trees

## What is a Tree?

A tree is a **non-linear data structure** used to represent data in a hierarchical way.

It starts with a single **root node**, and every node can have one or more child nodes.

Example:

```
      A
     / \
    B   C
   / \ / \
  D  E F  G
```


## Basic Terms

- **Root** → The first node of the tree.
- **Parent** → A node that has child nodes.
- **Child** → A node connected below a parent.
- **Leaf** → A node with no children.
- **Edge** → Connection between two nodes.


## Things to Remember

- Every tree has only one root.
- Each child has only one parent.
- Trees do not contain cycles.
- A tree with **n nodes** has **n - 1 edges**.



## Common Operations

| Operation | What it does |
|-----------|--------------|
| Traversal | Visit all nodes |
| Search | Find a node |
| Insert | Add a new node |
| Delete | Remove a node |



## Tree Traversals

- **Preorder** → Root → Left → Right
- **Inorder** → Left → Root → Right
- **Postorder** → Left → Right → Root
- **Level Order** → Visit nodes level by level (BFS)



## Advantages

- Good for representing hierarchical data.
- Searching is efficient in balanced trees.
- Easy to organize data.



## Where are Trees used?

- File systems
- Organization charts
- Database indexing
- Decision trees
- HTML/XML structure



## Quick Summary

- Hierarchical structure
- One root node
- No cycles
- Multiple traversal methods
- Used for searching and organizing data