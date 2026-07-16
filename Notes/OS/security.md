#  Disk Management, Linux, Security & Interview Preparation

# Table of Contents

1.  Disk Structure
2.  HDD vs SSD
3.  Disk Scheduling
4.  RAID
5.  Device Drivers
6.  Buffering, Caching & Spooling
7.  I/O Management
8.  Linux Basics
9.  Common Linux Commands
10. File Permissions
11. Shell & Bash
12. Virtualization
13. Containers vs Virtual Machines
14. Protection & Security
15. Authentication vs Authorization
16. Common OS Interview Questions
17. Quick Revision

# 1. Disk Structure

A disk stores data permanently even after power is turned off.

A traditional hard disk contains: - Platters - Tracks - Sectors -
Read/Write Head

Think of it like a circular notebook divided into rings (tracks) and
slices (sectors).

# 2. HDD vs SSD

  HDD            SSD
  -------------- -----------------
  Mechanical     Electronic
  Slower         Faster
  Cheaper        Costlier
  More noise     Silent
  Moving parts   No moving parts

Use SSDs for operating systems and frequently used applications.

# 3. Disk Scheduling

The OS decides the order in which disk requests are served.

## FCFS

Requests are served in arrival order.

Simple but not always efficient.

## SSTF

Shortest Seek Time First.

Chooses the closest request.

Fast but may cause starvation.

## SCAN

The disk head moves in one direction servicing requests, then reverses.

Also called the **Elevator Algorithm**.

## C-SCAN

Moves in one direction only.

Provides more uniform waiting time.

## LOOK

Similar to SCAN but only travels as far as the last request.

## C-LOOK

Circular version of LOOK.

# 4. RAID

RAID combines multiple disks.

Common levels:

-   RAID 0 → Performance
-   RAID 1 → Mirroring
-   RAID 5 → Performance + Fault Tolerance
-   RAID 10 → Mirroring + Striping

Remember: 0 = Speed 1 = Safety

# 5. Device Drivers

A device driver allows the operating system to communicate with
hardware.

Examples: - Printer driver - Graphics driver - Wi-Fi driver

Think of a driver as a translator between the OS and the hardware.

# 6. Buffering, Caching & Spooling

## Buffering

Temporarily stores data during transfer.

Example: Watching a YouTube video.

## Caching

Stores frequently used data for faster access.

Example: Browser cache.

## Spooling

Stores jobs in a queue.

Example: Printer queue.

Memory Trick: Buffer = Temporary Cache = Frequently Used Spool = Waiting
Queue

# 7. I/O Management

Input/Output management coordinates communication between hardware
devices and applications.

Responsibilities: - Device allocation - Interrupt handling - Error
handling - Driver management

# 8. Linux Basics

Linux is an open-source operating system widely used in servers and
cloud computing.

Popular distributions: - Ubuntu - Fedora - Debian - Arch Linux

# 9. Common Linux Commands

``` bash
pwd      # current directory
ls       # list files
cd       # change directory
mkdir    # create folder
rm       # remove file
cp       # copy
mv       # move
cat      # display file
touch    # create file
grep     # search text
find     # search files
ps       # running processes
top      # system monitor
kill     # terminate process
chmod    # change permissions
```

# 10. File Permissions

Linux permissions consist of:

-   Read (r)
-   Write (w)
-   Execute (x)

Example:

``` bash
chmod 755 app.sh
```

755 means: - Owner = rwx - Group = r-x - Others = r-x

# 11. Shell & Bash

The shell is a command interpreter.

Popular shells: - Bash - Zsh - Fish - PowerShell

Example:

``` bash
echo "Hello"
```

The shell converts commands into system calls.

# 12. Virtualization

Virtualization allows multiple operating systems to run on one physical
computer.

Examples: - VMware - VirtualBox - Hyper-V

Benefits: - Testing - Isolation - Better hardware utilization

# 13. Containers vs Virtual Machines

  Containers      Virtual Machines
  --------------- ------------------
  Share host OS   Separate OS
  Lightweight     Heavier
  Fast startup    Slower startup

Popular container platform: Docker.

# 14. Protection & Security

Protection controls access to resources.

Security protects against attacks.

Common principles: - Least Privilege - Access Control - Encryption -
Backups

# 15. Authentication vs Authorization

  Authentication   Authorization
  ---------------- ----------------------
  Who are you?     What can you access?

Example:

Login with password → Authentication

Opening admin dashboard → Authorization

# 16. Common OS Interview Questions

-   What happens when you boot a computer?
-   Process vs Thread?
-   User Mode vs Kernel Mode?
-   What is a System Call?
-   Explain Context Switching.
-   What is a Race Condition?
-   Mutex vs Semaphore?
-   What is Deadlock?
-   Paging vs Segmentation?
-   Virtual Memory?
-   FIFO vs LRU?
-   SSD vs HDD?
-   What is RAID?
-   What is a Device Driver?
-   Buffer vs Cache vs Spooling?
-   Containers vs Virtual Machines?

# 17. Quick Revision

-   HDD = Mechanical storage
-   SSD = Flash storage
-   SCAN = Elevator algorithm
-   RAID = Multiple disks
-   Driver = Hardware translator
-   Buffer = Temporary storage
-   Cache = Frequently accessed data
-   Spooling = Queue jobs
-   Linux = Open-source OS
-   Bash = Shell
-   Docker = Containers
-   Authentication = Identity
-   Authorization = Permission


