

## Introduction

One thing I learned about Linux is that it is designed to support multiple users. This means more than one person can use the same system, and each user can have their own files, settings, and permissions.

This is one of the reasons Linux is widely used on servers.

## Types of Users

There are mainly two types of users in Linux.

### Root User

The root user is the administrator of the system.

This user has complete control and can access or modify almost anything in Linux.

Because of these permissions, we should be careful while using the root account.

### Normal User

A normal user has limited permissions.

Most of the time, we log in as a normal user to keep the system safe. If we need to perform an administrative task, we can use `sudo`.

## What is sudo?

`sudo` stands for **SuperUser Do**.

It allows a normal user to run commands with administrator privileges.

Example:

```bash
sudo apt update
```

When I use `sudo`, Linux usually asks for my password before running the command.

## Checking the Current User

To know which user I'm logged in as:

```bash
whoami
```

Example output:

```text
deepthi
```

## Checking User Information

To see details about the current user:

```bash
id
```

This shows information like:

* User ID (UID)
* Group ID (GID)
* Groups the user belongs to

## Creating a New User

A new user can be created using:

```bash
sudo adduser john
```

Linux will ask for a password and a few optional details before creating the account.

## Changing a User's Password

To change a user's password:

```bash
sudo passwd john
```

Linux will ask for the new password.

If I want to change my own password, I can simply use:

```bash
passwd
```

## Switching Users

To switch to another user:

```bash
su john
```

To switch back to the root user:

```bash
sudo su
```

To return to the previous user:

```bash
exit
```

## Deleting a User

To remove a user account:

```bash
sudo deluser john
```

If I also want to remove the user's home directory:

```bash
sudo deluser --remove-home john
```

## What are Groups?

A group is a collection of users.

Instead of giving permissions to each user one by one, Linux allows us to assign permissions to a group.

This makes user management much easier, especially on systems with many users.

## Adding a User to a Group

To add a user to an existing group:

```bash
sudo usermod -aG developers john
```

Here:

* `-a` means append.
* `-G` means group.

This command adds **john** to the **developers** group.

## Viewing Groups

To see the groups of the current user:

```bash
groups
```

To check another user's groups:

```bash
groups john
```

## User's Home Directory

Every user has a personal home directory.

For example:

```text
/home/deepthi
```

or

```text
/home/john
```

This is where users usually store their personal files and projects.

## Useful User Management Commands

| Command   | Purpose                             |
| --------- | ----------------------------------- |
| `whoami`  | Shows the current user              |
| `id`      | Displays user and group information |
| `groups`  | Shows user groups                   |
| `sudo`    | Runs a command as an administrator  |
| `adduser` | Creates a new user                  |
| `passwd`  | Changes a password                  |
| `su`      | Switches to another user            |
| `deluser` | Deletes a user                      |
| `usermod` | Modifies a user account             |

## What I Learned

At first, I thought Linux only had one user like my personal computer. Later, I understood that Linux is built to handle multiple users safely.

The idea of having normal users and an administrator helps protect the system from accidental changes. I also learned that `sudo` is one of the most commonly used commands because it lets a normal user perform administrative tasks only when needed.

Overall, understanding users, groups, and permissions gave me a better idea of how Linux manages security.
