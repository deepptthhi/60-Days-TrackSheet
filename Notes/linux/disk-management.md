
## What is Disk Management?

Disk management is the process of managing your computer's storage. It helps you view disks, check available space, manage partitions, and mount or unmount storage devices.

Keeping an eye on disk usage helps prevent storage issues and keeps your system running smoothly.


## Checking Disk Space

To view the total and available disk space:

```bash
df -h
```

The `-h` option displays the size in a human-readable format (KB, MB, GB).

Example output:

```text
Filesystem      Size  Used  Avail  Use%
```

## Checking Folder Size

To find the size of a specific folder:

```bash
du -sh folder_name
```

Example:

```bash
du -sh Downloads
```

Options used:

- `-s` → Displays only the total size.
- `-h` → Shows the size in a readable format.


## Viewing Available Disks

To list all disks and partitions connected to your system:

```bash
lsblk
```

Example output:

```text
NAME   SIZE TYPE MOUNTPOINT
sda    100G disk
├─sda1  99G part /
└─sda2   1G part
```

This command helps you identify storage devices connected to your computer.


## Viewing Partition Information

To display detailed information about disks and partitions:

```bash
sudo fdisk -l
```

This command shows:

- Disk size
- Partitions
- File system type
- Partition table
## Understanding Storage Devices

In Linux, storage devices are represented as files under the `/dev` directory.

Some common names are:

- `/dev/sda` → First hard disk or SSD
- `/dev/sdb` → Second hard disk or SSD
- `/dev/sda1` → First partition of the first disk
- `/dev/sda2` → Second partition of the first disk

You can view all connected storage devices using:

```bash
lsblk
```
## What is a Partition?

A partition is a section of a physical disk.

Instead of using one large disk as a single storage space, it can be divided into multiple partitions. Each partition can have its own file system and can be mounted separately.

For example:

```text
Disk (500 GB)
│
├── Partition 1 (100 GB)
├── Partition 2 (200 GB)
└── Partition 3 (200 GB)
```
## Common File Systems

A file system decides how data is stored and organized on a storage device.

Some commonly used file systems are:

| File System | Used In |
|-------------|---------|
| ext4 | Most Linux distributions |
| xfs | Large storage systems |
| ntfs | Windows |
| vfat | USB drives and memory cards |

To check the file system type:

```bash
df -T
```

## Mounting a Disk

Before using a new storage device, it usually needs to be mounted.

Mount a disk:

```bash
sudo mount /dev/sdb1 /mnt
```

Here:

- `/dev/sdb1` → Storage device
- `/mnt` → Location where it will be accessible


## Unmounting a Disk

When you're done using a storage device, safely unmount it:

```bash
sudo umount /mnt
```

This ensures all data is properly written before removing the device.


## Checking File System Type

To see the file system used by each partition:

```bash
df -T
```

Common file systems include:

- ext4
- xfs
- ntfs
- vfat


## Useful Commands

```bash
df -h          # Check disk space
du -sh         # Check folder size
lsblk          # List disks and partitions
sudo fdisk -l  # View partition details
mount          # Mount a storage device
umount         # Unmount a storage device
df -T          # Show file system type
```


## Quick Summary

- Disk management helps manage storage devices and partitions.
- Use `df -h` to check available disk space.
- Use `du -sh` to check the size of a folder.
- Use `lsblk` to view disks and partitions.
- Use `fdisk -l` to see detailed partition information.
- Use `mount` to attach a storage device.
- Use `umount` to safely remove a mounted device.
- Use `df -T` to check the file system type.


## Commands to Remember

```bash
df -h
du -sh folder_name
lsblk
sudo fdisk -l
sudo mount /dev/sdb1 /mnt
sudo umount /mnt
df -T
```