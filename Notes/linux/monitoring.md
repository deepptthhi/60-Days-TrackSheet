

## What is System Monitoring?

System monitoring means checking how your Linux system is performing. It helps you keep track of things like CPU usage, memory usage, disk space, running processes, and overall system health.

Monitoring is useful because it helps you identify performance issues before they become serious.


## Checking CPU Usage

To monitor CPU usage and running processes in real time:

```bash
top
```

This shows:

- CPU usage
- Memory usage
- Running processes
- System load
- Uptime

To quit `top`, press:

```text
q
```


## Checking Memory Usage

To see how much RAM is being used:

```bash
free -h
```

The `-h` option displays the output in a human-readable format (MB, GB, etc.).

Example output:

```text
Total     Used     Free
```


## Checking Disk Space

To check available disk space:

```bash
df -h
```

It shows:

- Total disk space
- Used space
- Available space
- Mounted file systems


## Checking Folder Size

To find the size of a specific folder:

```bash
du -sh folder_name
```

Example:

```bash
du -sh Downloads
```

The `-s` option gives a summary, and `-h` displays the size in a readable format.


## Viewing Running Processes

To list currently running processes:

```bash
ps
```

To view all processes:

```bash
ps -ef
```


## Checking System Uptime

To see how long your system has been running:

```bash
uptime
```

It also displays the system load average.


## Viewing System Information

Display kernel and operating system information:

```bash
uname -a
```

Display the hostname (computer name):

```bash
hostname
```


## Checking Network Connections

To view active network connections and listening ports:

```bash
ss
```


## Useful Commands

```bash
top         # Monitor CPU and processes
free -h     # Check memory usage
df -h       # Check disk space
du -sh      # Check folder size
ps          # View running processes
ps -ef      # View all processes
uptime      # Show system uptime
uname -a    # System information
hostname    # Display system name
ss          # View network connections
```


## Quick Summary

- System monitoring helps you understand how your computer is performing.
- Use `top` to monitor CPU and running processes.
- Use `free -h` to check RAM usage.
- Use `df -h` to check available disk space.
- Use `du -sh` to check the size of a folder.
- Use `uptime` to see how long the system has been running.
- Use `ss` to view active network connections.


## Commands to Remember

```bash
top
free -h
df -h
du -sh folder_name
ps
ps -ef
uptime
uname -a
hostname
ss
```