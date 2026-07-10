

## What is a Process?

A **process** is simply a program that is currently running on your system.

For example, when you open VS Code, Chrome, or run a Python program, Linux creates a separate process for each one.

Every process has a unique **Process ID (PID)** which helps Linux identify and manage it.


## Viewing Running Processes

To see the processes running in the current terminal:

```bash
ps
```

To view all running processes:

```bash
ps -ef
```

This displays details like:

- PID (Process ID)
- User
- CPU usage
- Memory usage
- Command being executed


## Monitoring Processes

To monitor processes in real time:

```bash
top
```

It shows:

- Running processes
- CPU usage
- Memory usage
- System uptime
- Load average

To exit `top`, press:

```text
q
```

A more user-friendly version is:

```bash
htop
```

> **Note:** `htop` may need to be installed separately.


## Process States

A process can be in different states:

- **Running** – The process is currently using the CPU.
- **Sleeping** – Waiting for something to happen.
- **Stopped** – The process has been paused.
- **Zombie** – The process has finished but hasn't been completely removed yet.


## Killing a Process

If a program is frozen or taking too many resources, you can stop it.

First, find its PID:

```bash
ps -ef
```

Stop the process:

```bash
kill PID
```

Example:

```bash
kill 2456
```

Force stop a process:

```bash
kill -9 PID
```

Example:

```bash
kill -9 2456
```


## Running a Process in the Background

Normally, a command runs in the foreground.

To run it in the background, add `&` at the end.

Example:

```bash
python app.py &
```

Now you can continue using the terminal while the program runs.


## Managing Background Jobs

View background jobs:

```bash
jobs
```

Bring a background job back to the foreground:

```bash
fg
```

Send a running process to the background:

```bash
bg
```


## Process Priority

Linux allows you to control the priority of a process.

Start a process with a custom priority:

```bash
nice
```

Change the priority of an existing process:

```bash
renice
```

Higher priority processes usually get more CPU time.


## Useful Commands

```bash
ps          # Show running processes
ps -ef      # Show all processes
top         # Monitor processes
htop        # Better process monitor
kill        # Stop a process
kill -9     # Force stop a process
jobs        # View background jobs
fg          # Bring job to foreground
bg          # Continue job in background
nice        # Start process with priority
renice      # Change process priority
```


## Quick Summary

- A **process** is a running program.
- Every process has a unique **PID (Process ID)**.
- Use `ps` to view running processes.
- Use `top` or `htop` to monitor CPU and memory usage.
- Use `kill` to stop a process.
- Add `&` to run a command in the background.
- Use `jobs`, `fg`, and `bg` to manage background processes.
- `nice` and `renice` help control process priority.


## Commands to Remember

```bash
ps
ps -ef
top
htop
kill PID
kill -9 PID
jobs
fg
bg
python app.py &
nice
renice
```