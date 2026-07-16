

# Processes, Threads & CPU Scheduling



# 1. Program vs Process

## What is a Program?

A **program** is a set of instructions stored on disk.

Examples: - Chrome.exe - VS Code - Spotify

A program is **passive** because it is not running.

## What is a Process?

A **process** is a program that is currently running.

Example: When you double-click Chrome, the program becomes a process.

## Real-life Example

Recipe = Program

Cooking = Process

## How to Remember

**Program = Stored** **Process = Running**

# 2. Process Lifecycle

A process goes through several stages:

New → Ready → Running → Waiting → Ready → Running → Terminated

Explanation: - New: Process created. - Ready: Waiting for CPU. -
Running: Executing. - Waiting: Waiting for I/O. - Terminated: Finished.

## Real-life Example

A student: - Arrives at exam hall - Waits outside - Writes exam - Waits
for answer sheet collection - Leaves

# 3. Process States

  State        Meaning
  ------------ -------------------
  New          Created
  Ready        Waiting for CPU
  Running      Using CPU
  Waiting      Waiting for event
  Terminated   Finished

# 4. Process Control Block (PCB)

A PCB stores all information about a process.

Contains: - Process ID (PID) - Process State - CPU Registers - Program
Counter - Scheduling Information - Memory Information - Open Files

## Why do we need it?

If the CPU switches to another process, the OS saves everything in the
PCB.

## Memory Trick

**PCB = Identity Card of a Process**

# 5. Context Switching

Context Switching happens when the CPU switches from one process to
another.

Steps: 1. Save Process A information in PCB. 2. Load Process B
information. 3. Resume Process B.

## Example

You're studying OS. Your friend calls. You answer. Later you continue
exactly where you stopped.

That's context switching.

## Drawback

Too many context switches reduce performance because saving and
restoring state takes time.

# 6. Process Creation

In Linux, a new process is commonly created using:

-   fork()
-   exec()

Example:

``` c
pid_t pid = fork();

if(pid == 0){
    printf("Child Process");
}else{
    printf("Parent Process");
}
```

fork() creates a copy of the current process.

exec() replaces the current process with a new program.

# 7. Process Termination

A process ends when:

-   Work completes
-   Error occurs
-   Parent terminates it
-   User closes application

Example: Closing Notepad ends its process.

# 8. Zombie, Orphan & Daemon Processes

## Zombie Process

A process has finished execution, but its entry still exists because the
parent hasn't collected its exit status.

Remember: Zombie = Dead but entry remains.

## Orphan Process

Parent finishes first.

Child continues running.

Linux assigns the child to the init/systemd process.

Remember: Orphan = Parent missing.

## Daemon Process

Runs in the background.

Examples: - Web server - Print service - SSH server

Remember: Daemon = Background helper.

# 9. Threads

A thread is the smallest unit of CPU execution.

One process can contain multiple threads.

Example: Chrome - UI Thread - Rendering Thread - Download Thread

## Process vs Thread

  Process           Thread
  ----------------- -----------------
  Heavyweight       Lightweight
  Separate memory   Shared memory
  Slower creation   Faster creation

## Real-life Example

House = Process

Family members = Threads

Everyone shares the same house.

# 10. Multithreading Models

-   Many-to-One
-   One-to-One
-   Many-to-Many

One-to-One is commonly used in modern systems.

Benefits: - Better responsiveness - Better CPU utilization - Faster
applications

# 11. CPU Scheduling

The scheduler decides which process gets CPU next.

Goals: - High CPU utilization - Low waiting time - Low turnaround time -
Good response time

# 12. Scheduling Algorithms

## FCFS

First process arrives, first executes.

Pros: - Simple

Cons: - Convoy effect

## SJF

Shortest job executes first.

Pros: - Minimum average waiting time.

Cons: - Difficult to predict burst time.

## SRTF

Preemptive version of SJF.

Shorter job can interrupt the running one.

## Priority Scheduling

Higher priority executes first.

Problem: Starvation.

## Round Robin

Each process gets a fixed time quantum.

Example: 20 ms each.

Best for interactive systems.

## Multilevel Queue

Separate queues for different process types.

## Multilevel Feedback Queue

Processes can move between queues.

One of the most flexible scheduling algorithms.

# 13. Dispatcher

The dispatcher gives CPU control to the selected process.

Responsibilities: - Context switch - Switch to user mode - Start
execution

# 14. Starvation & Aging

## Starvation

Low-priority process waits indefinitely.

## Aging

Gradually increase waiting process priority.

Memory Trick:

Aging prevents starvation.

# 15. Quick Revision

-   Program = Stored instructions
-   Process = Running program
-   PCB = Process information
-   Thread = Smallest execution unit
-   Context Switch = CPU changes process
-   Zombie = Finished but not cleaned
-   Orphan = Parent ended first
-   Daemon = Background service
-   Scheduler = Chooses next process
-   Dispatcher = Gives CPU

