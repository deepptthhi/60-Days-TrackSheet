

## Introduction

After understanding the Linux folder structure, the next step was learning how to work with files and folders using commands.

At first, it felt strange because I was used to clicking with a mouse. But after practicing a few commands, I realized that using the terminal is actually faster.

## Finding My Current Location

Before doing anything, it's useful to know where I am in the file system.

The `pwd` command shows the current directory.

```bash
pwd
```

Example output:

```text
/home/deepthi
```

## Listing Files and Folders

The `ls` command shows everything inside the current folder.

```bash
ls
```

If I want more details like permissions, owner, and file size, I can use:

```bash
ls -l
```

To see hidden files as well:

```bash
ls -a
```

## Moving Between Folders

The `cd` command is used to change directories.

Go into a folder:

```bash
cd Documents
```

Go back one folder:

```bash
cd ..
```

Go directly to the home directory:

```bash
cd ~
```

Go to the root directory:

```bash
cd /
```

## Creating a Folder

To create a new folder, I use the `mkdir` command.

```bash
mkdir Projects
```

If I want to create folders inside folders in one command:

```bash
mkdir -p College/Notes/Linux
```

## Creating a File

The easiest way to create an empty file is:

```bash
touch notes.txt
```

I can create multiple files at once.

```bash
touch file1.txt file2.txt file3.txt
```

## Viewing File Content

To read the contents of a file:

```bash
cat notes.txt
```

If the file is very long, these commands are more useful:

```bash
less notes.txt
```

or

```bash
more notes.txt
```

## Copying Files

To copy a file:

```bash
cp notes.txt backup.txt
```

To copy a folder:

```bash
cp -r Projects Backup
```

The `-r` option means **recursive**, which copies everything inside the folder.

## Moving or Renaming Files

The `mv` command is used for both moving and renaming.

Rename a file:

```bash
mv old.txt new.txt
```

Move a file to another folder:

```bash
mv notes.txt Documents/
```

## Deleting Files

To delete a file:

```bash
rm notes.txt
```

To delete an empty folder:

```bash
rmdir Test
```

To delete a folder with everything inside it:

```bash
rm -r Projects
```

I always double check before using `rm` because deleted files cannot be easily recovered.

## Searching for Files

If I don't remember where a file is, I can use the `find` command.

```bash
find . -name notes.txt
```

This searches for the file in the current directory and its subfolders.

## Wildcards

Wildcards help when working with multiple files.

`*` means **anything**.

Example:

```bash
ls *.txt
```

This lists all `.txt` files.

`?` represents a single character.

Example:

```bash
ls file?.txt
```

This matches files like:

* file1.txt
* file2.txt
* fileA.txt

## File Permissions (Basic Idea)

Every file in Linux has permissions.

These permissions decide:

* Who can read the file
* Who can edit it
* Who can execute it

I don't need to memorize everything right now. For now, it's enough to know that Linux uses permissions to keep files secure.

I'll learn permission commands like `chmod` and `chown` in more detail later.

## Commands I Practiced

| Command | Purpose                  |
| ------- | ------------------------ |
| `pwd`   | Shows current directory  |
| `ls`    | Lists files and folders  |
| `cd`    | Changes directory        |
| `mkdir` | Creates a folder         |
| `touch` | Creates a file           |
| `cat`   | Displays file content    |
| `cp`    | Copies files and folders |
| `mv`    | Moves or renames files   |
| `rm`    | Deletes files            |
| `rmdir` | Deletes an empty folder  |
| `find`  | Searches for files       |

## What I Learned

Learning file management made me feel much more comfortable using Linux.

At first, I kept forgetting the commands, but after using them a few times, they started becoming familiar. I also realized that most Linux work is just moving around folders, creating files, copying them, and deleting them.

The more I practice these commands, the more natural they feel.
