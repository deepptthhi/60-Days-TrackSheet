# Queues

## What is a Queue?

A queue is a linear data structure that follows the **FIFO (First In, First Out)** principle.

The first element added is also the first one to be removed.

Think of people standing in a queue. The person who comes first gets served first.

Example:

```
Front → 10 20 30 40 50 ← Rear
```



## Things to Remember

- Elements are added from the rear.
- Elements are removed from the front.
- Follows the FIFO rule.



## Common Operations

| Operation | What it does | Time |
|-----------|--------------|------|
| Enqueue | Add an element | O(1) |
| Dequeue | Remove the front element | O(1) |
| Front | View the first element | O(1) |
| Rear | View the last element | O(1) |



## Advantages

- Maintains the correct processing order.
- Fast insertion and deletion.



## Disadvantages

- No direct access to middle elements.
- Less flexible compared to arrays.



## Where are Queues used?

- CPU scheduling
- Printer queues
- Handling requests in servers
- Breadth First Search (BFS)



## Quick Summary

- Follows FIFO
- Insert from Rear
- Delete from Front
- Used for scheduling and request processing