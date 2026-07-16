# Advanced & Frequently Missed Topics

These topics are often skipped in short OS notes but are useful for
placements, GATE basics, and interviews.

## Process Management

-   Process Scheduling Queue
-   Long-term, Short-term & Medium-term Scheduler
-   CPU Burst vs I/O Burst
-   Dispatcher Latency
-   Process Hierarchy
-   Process Image
-   Reentrant Code

## Threads

-   Thread Safety
-   Thread Local Storage (TLS)
-   Thread Synchronization
-   Thread Cancellation

## CPU Scheduling

-   Turnaround Time
-   Waiting Time
-   Response Time
-   Throughput
-   CPU Utilization
-   Convoy Effect
-   Preemptive vs Non-preemptive Scheduling

## Synchronization

-   Busy Waiting
-   Spinlocks
-   Atomic Operations
-   Compare-and-Swap (CAS)
-   Test-and-Set
-   Memory Barriers
-   Condition Variables

## Deadlocks

-   Resource Allocation Graph (RAG)
-   Safe State vs Unsafe State
-   Safe Sequence
-   Deadlock Detection Algorithm

## Memory Management

-   Dynamic Loading
-   Dynamic Linking
-   Overlay
-   Compaction
-   Buddy System
-   Slab Allocation
-   Huge Pages
-   NUMA (overview)

## Virtual Memory

-   Page Tables
-   Multi-level Page Tables
-   Inverted Page Tables
-   Hashed Page Tables
-   Copy-on-Write (COW)
-   Memory-Mapped Files (mmap)
-   Working Set Model
-   Effective Access Time (EAT)

## File Systems

-   Hard Link vs Soft Link
-   Mounting
-   Boot Block
-   Superblock
-   File Descriptors
-   Access Control Lists (ACL)
-   Symbolic Links

## Disk Management

-   Seek Time
-   Rotational Latency
-   Transfer Time
-   Disk Cache
-   Bad Block Recovery

## I/O Systems

-   Polling
-   Interrupt-driven I/O
-   Memory-mapped I/O
-   Programmed I/O
-   Synchronous vs Asynchronous I/O

## Security

-   Access Matrix
-   Capability Lists
-   Domain of Protection
-   Secure Boot
-   TPM (overview)
-   SELinux/AppArmor (overview)

## Linux

-   init vs systemd
-   Cron Jobs
-   Environment Variables
-   Pipes and Redirection
-   awk
-   sed
-   xargs
-   tar
-   zip
-   gzip
-   curl
-   wget
-   ssh
-   scp

## Modern Operating Systems

-   Android Architecture
-   iOS Architecture
-   Windows Architecture
-   Linux Kernel Architecture
-   Hypervisors (Type 1 & Type 2)
-   Docker Internals
-   Kubernetes (high-level)
-   WSL (Windows Subsystem for Linux)

# Frequently Asked Interview Comparisons

-   Program vs Process
-   Process vs Thread
-   User Thread vs Kernel Thread
-   User Mode vs Kernel Mode
-   Mutex vs Semaphore
-   Binary vs Counting Semaphore
-   Paging vs Segmentation
-   HDD vs SSD
-   BIOS vs UEFI
-   Authentication vs Authorization
-   Containers vs Virtual Machines
-   Hard Link vs Soft Link
-   Polling vs Interrupt
-   Cache vs Buffer vs Spooling

# Practice Worth Doing

-   Draw Process State Diagram
-   Draw Paging Address Translation
-   Solve Page Replacement Problems
-   Solve Disk Scheduling Numericals
-   Solve Banker's Algorithm
-   Explain Boot Process
-   Explain Context Switching
-   Explain Virtual Memory using an example

# Additional Theory Topics (Complete Coverage)

> This appendix lists the remaining Operating Systems theory topics that
> are commonly covered in university courses, GATE syllabi, and software
> engineering interviews. It complements the first five handbook files.

# 1. Advanced Process Management

## Scheduling Queues

-   Job Queue
-   Ready Queue
-   Device Queue

## Types of Schedulers

-   Long-Term Scheduler
-   Medium-Term Scheduler
-   Short-Term Scheduler

## Other Concepts

-   CPU-bound vs I/O-bound Processes
-   Process Image
-   Reentrant Code

# 2. Advanced Memory Management

## Program Loading

-   Dynamic Loading
-   Dynamic Linking
-   Shared Libraries

## Memory Allocation

-   First Fit
-   Best Fit
-   Worst Fit
-   Next Fit

## Memory Organization

-   Compaction
-   Relocation
-   Memory Protection
-   Buddy Memory Allocation
-   Slab Allocation (overview)

# 3. Advanced Virtual Memory

## Page Tables

-   Single-Level Page Table
-   Multi-Level Page Table
-   Inverted Page Table
-   Hashed Page Table (overview)

## Other Concepts

-   Copy-on-Write (COW)
-   Memory-Mapped Files (mmap)
-   Working Set Model
-   Local Page Replacement
-   Global Page Replacement
-   Effective Access Time (EAT)

# 4. Advanced File Systems

## Internal Structures

-   Boot Block
-   Superblock
-   File Descriptors
-   Virtual File System (VFS)

## File Management

-   Mounting
-   Unmounting
-   Hard Links
-   Soft (Symbolic) Links
-   Access Control Lists (ACL)

# 5. Advanced I/O System

## I/O Techniques

-   Programmed I/O
-   Interrupt-Driven I/O
-   DMA I/O

## Communication Styles

-   Polling
-   Synchronous I/O
-   Asynchronous I/O
-   Blocking I/O
-   Non-Blocking I/O

# 6. Advanced Protection & Security

## Protection

-   Protection Domains
-   Access Matrix
-   Capability Lists

## Security

-   Security Policies
-   Secure Boot
-   Trusted Platform Module (TPM)

# 7. Modern Operating System Concepts

## Hardware & Memory

-   NUMA (Non-Uniform Memory Access)

## Virtualization

-   Hypervisors
    -   Type 1
    -   Type 2

## Linux Internals

-   Linux Kernel Modules
-   cgroups
-   Namespaces

## Containers

-   Container Internals
-   Docker Architecture

## Modern Platforms

-   Windows Subsystem for Linux (WSL)
-   Android Architecture
-   iOS Architecture

# 8. Advanced Academic Topics

-   Demand Segmentation
-   Segmented Paging
-   Working Set Algorithm
-   Clock-Pro Algorithm
-   Huge Pages
-   Buddy vs Slab Allocator (comparison)
-   Extent-Based Allocation
-   Journaling Internals
-   Log-Structured File Systems
-   Distributed File Systems
-   Network File System (NFS)
-   Andrew File System (AFS)
-   Distributed Operating Systems
-   Cluster Operating Systems
-   Embedded Operating Systems
-   Mobile Operating Systems

# 9. Real-Time Operating Systems

## Scheduling Algorithms

-   Rate Monotonic Scheduling (RMS)
-   Earliest Deadline First (EDF)

## Characteristics

-   Deterministic execution
-   Low latency
-   Predictable response
-   Deadline guarantees

# 10. Optional Deep-Dive Topics

These are generally beyond placement interview requirements but useful
for advanced study.

-   Exokernel
-   Nanokernel
-   Capability-Based Operating Systems
-   Scheduler Activations
-   Linux Completely Fair Scheduler (CFS)
-   Windows NT Architecture Internals
-   ext4 Internal Design
-   Mach Kernel IPC
-   Barrelfish Operating System
-   Firecracker MicroVMs

# Recommended Study Order

1.  Fundamentals
2.  Processes & Threads
3.  CPU Scheduling
4.  Synchronization
5.  Deadlocks
6.  Memory Management
7.  Virtual Memory
8.  File Systems
9.  Disk & I/O
10. Linux
11. Security
12. Modern OS Concepts
13. Advanced Topics (optional)



