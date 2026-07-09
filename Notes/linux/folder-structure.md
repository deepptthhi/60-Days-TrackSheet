
## Introduction

One thing I found interesting about Linux is that everything is organized inside folders. Unlike Windows, where we usually work with drives like **C:** or **D:**, Linux starts from a single main directory called the **root directory**.

Every file and folder in Linux comes under this root directory.

## What is the Root Directory?

The root directory is represented by a single forward slash:

```bash
/
```

It is the top most directory in Linux.

Every other folder is stored inside it.

A simple way to think about it is:

```text
/
├── home
├── bin
├── etc
├── usr
├── var
├── tmp
├── opt
├── dev
├── proc
└── boot
```

Everything starts from `/`.

## /home

The **home** folder stores personal files of users.

Every user gets their own folder inside `/home`.

For example:

```bash
/home/deepthi
```

This is usually where I save my files, projects, and documents.

## /bin

The **bin** folder contains basic Linux commands that we use every day.

Commands like:

* `ls`
* `cp`
* `mv`
* `cat`
* `pwd`

are available because of this directory.

## /etc

This folder contains configuration files.

Whenever we install software or change system settings, many configuration files are stored here.

I like to remember it as the **settings folder** of Linux.

## /usr

The `/usr` directory contains applications, libraries, and programs installed on the system.

Many software packages keep their files here.

Even though the name says **usr**, it actually stores a lot of system software.

## /var

The word **var** stands for **variable**.

This folder stores files that keep changing, such as:

* Log files
* Cache
* Mail
* Temporary data created by applications

Whenever I want to check logs, this is one of the important folders.

## /tmp

This folder stores temporary files.

Applications use it while they are running.

Many of these files are removed automatically after restarting the system.

## /opt

The `/opt` folder is used for optional or third-party software.

Some applications that are installed manually keep their files here.

## /dev

The `/dev` directory contains device files.

Linux treats hardware devices like files.

Things like:

* Keyboard
* Mouse
* Hard disk
* USB drive

can all be accessed through this directory.

## /proc

This folder is a little different.

It doesn't actually store files on the hard disk.

Instead, it provides information about the running system, processes, CPU, and memory.

The data is generated while the system is running.

## /boot

The `/boot` folder contains files needed when Linux starts.

Without these files, the operating system cannot boot properly.

## How I Remember These Folders

Instead of memorizing everything, I try to remember what each folder is mainly used for.

| Folder  | Easy way to remember        |
| ------- | --------------------------- |
| `/`     | Starting point of Linux     |
| `/home` | My personal files           |
| `/bin`  | Basic commands              |
| `/etc`  | System settings             |
| `/usr`  | Installed programs          |
| `/var`  | Files that keep changing    |
| `/tmp`  | Temporary files             |
| `/opt`  | Optional software           |
| `/dev`  | Hardware devices            |
| `/proc` | System information          |
| `/boot` | Files needed to start Linux |

## Useful Commands

Show the current folder:

```bash
pwd
```

List files and folders:

```bash
ls
```

Move into another folder:

```bash
cd folder_name
```

Go back one folder:

```bash
cd ..
```

Go to the home directory:

```bash
cd ~
```

Go to the root directory:

```bash
cd /
```

## What I Learned

At first, all these folders looked confusing because their names were short. But after understanding what each one is used for, they started making sense.

I don't try to memorize every folder. Instead, I remember the purpose of the important ones. With regular practice, navigating through the Linux file system becomes much easier.
