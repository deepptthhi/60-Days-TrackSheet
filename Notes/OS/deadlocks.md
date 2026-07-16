# Synchronization, Deadlocks & IPC


# 1. Why Process Synchronization?

When multiple processes or threads access the same data at the same
time, the result can become incorrect.

## Real-life Example

Imagine two cashiers updating the same bank account simultaneously.
Without coordination, the final balance could be wrong.

## How to Remember

**Synchronization = Coordination**

# 2. Race Condition

A race condition happens when the output depends on which process
finishes first.

Example:

Thread A reads balance = ₹1000.

Thread B also reads balance = ₹1000.

Both add ₹500.

Expected = ₹2000

Actual may become ₹1500.

The problem occurs because both updated the same value simultaneously.

# 3. Critical Section Problem

The **critical section** is the part of a program where shared resources
are accessed.

Only one process should execute inside the critical section at a time.

Requirements: - Mutual Exclusion - Progress - Bounded Waiting

Memory Trick:

**MPB** - Mutual Exclusion - Progress - Bounded Waiting

# 4. Peterson's Algorithm

Peterson's Algorithm is a software solution for two processes.

It uses: - flag\[\] - turn

It guarantees mutual exclusion for two processes.

Best suited for learning and interviews rather than modern operating
systems.

# 5. Hardware Synchronization

Modern processors provide atomic instructions like:

-   Test-and-Set
-   Compare-and-Swap (CAS)

These instructions help prevent race conditions efficiently.

# 6. Mutex

A mutex is a locking mechanism.

One thread locks the resource.

Other threads must wait.

Real-life Example:

One bathroom key.

Only one person can use it at a time.

Remember:

**Mutex = One key**

# 7. Semaphore

A semaphore controls access to shared resources.

Types:

## Binary Semaphore

Only values: 0 or 1

Works similar to a mutex.

## Counting Semaphore

Can have values greater than one.

Example:

Parking lot with 50 spaces.

If spaces become zero, incoming cars wait.

Memory Trick:

Semaphore = Traffic Signal

# 8. Monitor

A monitor is a high-level synchronization construct.

It automatically ensures that only one thread executes monitor code at a
time.

Languages like Java provide monitor support using synchronized blocks.

# 9. Classical Synchronization Problems

## Producer Consumer

Producer creates data.

Consumer uses data.

Shared buffer must not overflow or underflow.

## Readers Writers

Many readers can read simultaneously.

Only one writer can modify data.

## Dining Philosophers

Five philosophers share five forks.

Improper synchronization may lead to deadlock.

Purpose: Understand resource allocation problems.

# 10. Deadlocks

A deadlock occurs when two or more processes wait forever for resources
held by each other.

Real-life Example

Person A has Key 1 and wants Key 2.

Person B has Key 2 and wants Key 1.

Nobody can continue.

# 11. Deadlock Handling

## Coffman Conditions

All four must exist.

-   Mutual Exclusion
-   Hold and Wait
-   No Preemption
-   Circular Wait

Memory Trick:

**MHNC**

## Prevention

Break one Coffman condition.

## Avoidance

Allocate resources carefully.

Example: Banker's Algorithm.

## Detection

Allow deadlock to occur.

Later detect it.

## Recovery

Recover by: - Killing processes - Releasing resources

# 12. Banker's Algorithm

Used for deadlock avoidance.

Idea:

Grant resources only if the system remains in a safe state.

Important Terms:

-   Available
-   Allocation
-   Maximum
-   Need
-   Safe Sequence

Interview Tip:

Remember the formula:

Need = Maximum − Allocation

# 13. Inter Process Communication (IPC)

Processes often need to exchange data.

IPC provides communication mechanisms.

Methods: - Pipes - Shared Memory - Message Queue - Signals - Sockets

# 14. Pipes

A pipe transfers data between processes.

Anonymous Pipe: Parent ↔ Child

Named Pipe (FIFO): Unrelated processes can communicate.

Real-life Example:

Water pipe carrying information.

# 15. Shared Memory

Multiple processes share one memory area.

Advantages: - Extremely fast

Disadvantages: - Requires synchronization

# 16. Message Queues

Processes communicate by sending messages.

Advantages: - Easy communication - Independent execution

# 17. Signals

Signals notify a process that an event has occurred.

Examples:

SIGINT

Ctrl + C

SIGKILL

Immediately terminate a process.

SIGSTOP

Pause execution.

# 18. Sockets

Sockets enable communication over networks.

Examples: - Chat applications - Browsers - Web servers - Multiplayer
games

Think of sockets as communication endpoints.

# 19. Quick Revision

-   Synchronization = Coordination
-   Race Condition = Incorrect simultaneous access
-   Critical Section = Shared resource code
-   Mutex = One lock
-   Semaphore = Counter
-   Monitor = High-level synchronization
-   Deadlock = Waiting forever
-   Banker's Algorithm = Deadlock avoidance
-   Pipes = Data transfer
-   Shared Memory = Fast IPC
-   Signals = Notifications
-   Sockets = Network communication

