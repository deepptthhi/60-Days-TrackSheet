
## What are File Permissions?

Linux is a multi user operating system, which means multiple users can use the same system. File permissions decide **who can access a file or folder and what they are allowed to do with it**. They help keep files secure and prevent unauthorized changes.

## Types of Users

Every file or directory has permissions for three types of users.

### User (u)
The owner of the file.

### Group (g)
Users who belong to the same group.

### Others (o)
Everyone else who has access to the system.

Example:

```bash
-rwxr-xr--
```

Here:

- User → `rwx`
- Group → `r-x`
- Others → `r--`

## Permission Types

Linux has three basic permissions.

| Permission | Meaning |
|------------|---------|
| `r` | Read the file |
| `w` | Write or modify the file |
| `x` | Execute or run the file |

For directories:

- **Read (`r`)** → View the files inside the directory.
- **Write (`w`)** → Create, delete or rename files.
- **Execute (`x`)** → Enter or access the directory.

## Viewing File Permissions

Use the following command to check file permissions:

```bash
ls -l
```

Example:

```bash
-rw-r--r-- 1 user user 250 Jul 10 notes.txt
```

The first part (`-rw-r--r--`) shows the permissions.

## Changing Permissions (`chmod`)

The `chmod` command is used to change permissions.

Give execute permission to the owner:

```bash
chmod u+x script.sh
```

Remove write permission from the group:

```bash
chmod g-w script.sh
```

Give read permission to others:

```bash
chmod o+r script.sh
```

## Numeric Permissions

Permissions can also be represented using numbers.

| Permission | Value |
|------------|------:|
| Read | 4 |
| Write | 2 |
| Execute | 1 |

The values are added together.

Example:

```bash
chmod 755 script.sh
```

Meaning:

- Owner → `rwx`
- Group → `r-x`
- Others → `r-x`

Another example:

```bash
chmod 644 notes.txt
```

Meaning:

- Owner → `rw-`
- Group → `r--`
- Others → `r--`

## Changing Ownership

Change the owner of a file:

```bash
sudo chown username file.txt
```

Change both owner and group:

```bash
sudo chown username:groupname file.txt
```

Change only the group:

```bash
chgrp groupname file.txt
```

## Useful Commands

```bash
ls -l          # View permissions
chmod          # Change permissions
chown          # Change file owner
chgrp          # Change file group
```

## Quick Summary

- File permissions control who can access files and folders.
- There are three types of users: **User, Group and Others**.
- The three permissions are **Read (r), Write (w) and Execute (x)**.
- Use `ls -l` to view permissions.
- Use `chmod` to change permissions.
- Use `chown` to change the owner.
- Use `chgrp` to change the group.

## Commands to Remember

```bash
ls -l
chmod u+x file
chmod 755 file
chmod 644 file
sudo chown username file
chgrp groupname file
```