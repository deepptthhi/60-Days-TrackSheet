# Arrays

## What are Arrays?

An array is one of the simplest data structures.

It stores a group of values of the **same data type** in continuous
memory locations.

Think of it like a row of lockers. Every locker has a number (index), so
if you know the index, you can directly reach that element without
checking the others.

Example:

``` text
Index : 0   1   2   3   4
Array : 10  20  30  40  50
```



## Why do we use Arrays?

Instead of creating many variables like:

``` python
student1 = "A"
student2 = "B"
student3 = "C"
```

we can store everything in a single array:

``` python
students = ["A", "B", "C"]
```

This makes the code easier to write, read, and manage.



## Things to Remember

-   Stores only one type of data (in DSA).
-   Elements are stored next to each other in memory.
-   Index starts from **0**.
-   Size is usually fixed after creation (except dynamic arrays like
    Python lists).
-   Accessing an element is very fast because we already know its index.



## Types of Arrays

-   **1D Array** -- Stores elements in a single row.
-   **2D Array** -- Stores data in rows and columns (matrix).
-   **Multi-dimensional Array** -- More than two dimensions.
-   **Static Array** -- Fixed size after creation.
-   **Dynamic Array** -- Size can grow or shrink (Python list).



## Declaration & Initialization

``` python
arr = []
```

``` python
arr = [10, 20, 30]
```



## Indexing

``` python
arr = [10, 20, 30]

print(arr[0])   # 10
print(arr[-1])  # 30
```

Positive indexing starts from the beginning, while negative indexing
starts from the end.



## Traversing an Array

``` python
for num in arr:
    print(num)
```

or

``` python
for i in range(len(arr)):
    print(arr[i])
```

**Time Complexity:** O(n)



## Updating an Element

``` python
arr[1] = 100
```

**Time Complexity:** O(1)

## Common Operations

  Operation                What it does                     Time
  ------------------------ -------------------------------- ------
  Access                   Get an element using its index   O(1)
  Search (Linear Search)   Find an element                  O(n)
  Insert                   Add an element                   O(n)
  Delete                   Remove an element                O(n)
  Update                   Change an element                O(1)

> **Binary Search:** Works only on **sorted arrays** and takes **O(log
> n)** time.



## Advantages

-   Fast access to elements.
-   Easy to understand and implement.
-   Uses memory efficiently.
-   Great for storing large amounts of similar data.



## Disadvantages

-   Size cannot be changed easily in static arrays.
-   Insertion and deletion are expensive because elements may need to be
    shifted.
-   Requires continuous memory.



## Array vs Python List

  Array            Python List
  ---------------- ----------------------------
  Fixed size       Dynamic size
  Same data type   Can store mixed data types
  Less flexible    More flexible

> In Python DSA, we mostly use **lists**, which behave like dynamic
> arrays.



## Array vs Linked List

  -----------------------------------------------------------------------
  Array                       Linked List
  --------------------------- -------------------------------------------
  Fast random access (O(1))   Random access is O(n)

  Slow insertion/deletion in  Easier insertion/deletion once the node is
  middle                      known
  -----------------------------------------------------------------------



## Where are Arrays used?

-   Storing marks, IDs, salaries, etc.
-   Matrices
-   Image processing
-   Building other data structures like stacks, queues, and heaps


## Common Beginner Mistakes

-   Forgetting that indexing starts from **0**.
-   Accessing an invalid index.
-   Using Binary Search on an unsorted array.
-   Confusing `append()` with `insert()`.



## Quick Summary

-   Same data type
-   Continuous memory
-   Fast access (O(1))
-   Fixed size (except dynamic arrays)
-   Slow insertion and deletion (O(n))
-   Binary Search requires a sorted array
-   Python uses **lists** as dynamic arrays
