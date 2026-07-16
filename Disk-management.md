# Disk Management Commands

## 1. df (Disk Free)

### Purpose

Displays the total, used, and available disk space of mounted file systems.

### Syntax

```bash
df
```

Human-readable format

```bash
df -h
```

### Example

```bash
df -h
```

### Sample Output

```text
Filesystem      Size  Used Avail Use%
/dev/sda1       100G   40G   60G  40%
```

### Explanation

The `df` command shows the available and used storage space for each mounted filesystem.

---

## 2. du (Disk Usage)

### Purpose

Shows the size of files and directories.

### Syntax

```bash
du
```

Human-readable

```bash
du -h
```

Directory size only

```bash
du -sh Documents
```

### Example

```bash
du -sh Downloads
```

### Explanation

`du` calculates how much disk space a specific directory or file occupies.

---

## Difference between df and du

| df | du |
|----|----|
| Shows entire disk usage | Shows folder/file size |
| Filesystem based | Directory based |

---

## 3. lsblk

### Purpose

Lists all available block storage devices.

### Syntax

```bash
lsblk
```

### Sample Output

```text
NAME   SIZE TYPE
sda    512G disk
├─sda1 100G part
├─sda2 300G part
└─sda3 112G part
```

### Explanation

Useful for viewing disks, partitions, and attached storage devices.

---

## 4. blkid

### Purpose

Displays block device information including UUID and filesystem type.

### Syntax

```bash
sudo blkid
```

### Example Output

```text
/dev/sda1: UUID="A12B-34CD" TYPE="ext4"
```

---

## 5. fdisk

### Purpose

Creates, deletes, and manages disk partitions.

### List Partitions

```bash
sudo fdisk -l
```

### Explanation

Used for partition management on Linux systems.

---

## Summary

| Command | Purpose |
|----------|---------|
| df | Show disk space |
| du | Show directory size |
| lsblk | List block devices |
| blkid | Show filesystem information |
| fdisk | Manage partitions |

---

# Interview Questions

### Q1. Difference between df and du?

| df | du |
|----|----|
| Disk Usage | Directory Usage |

---

### Q2. Which command lists all block devices?

```bash
lsblk
```

---

### Q3. Which command displays filesystem UUID?

```bash
blkid
```

---

### Q4. Which command manages partitions?

```bash
fdisk
```

---

---

# 6. mount

## Purpose

The `mount` command is used to attach a storage device or filesystem to a directory.

### Syntax

```bash
sudo mount device directory
```

### Example

```bash
sudo mount /dev/sdb1 /mnt
```

### Explanation

After mounting, the files on the storage device become accessible through the specified directory.

---

# 7. umount

## Purpose

The `umount` command is used to safely detach a mounted filesystem.

### Syntax

```bash
sudo umount /mnt
```

or

```bash
sudo umount /dev/sdb1
```

### Explanation

Always unmount a storage device before removing it to prevent data corruption.

---

# 8. mkfs

## Purpose

Creates a new filesystem on a partition.

### Syntax

```bash
sudo mkfs -t ext4 /dev/sdb1
```

### Example

```bash
sudo mkfs.ext4 /dev/sdb1
```

### Explanation

This command formats the partition and prepares it for storing files.

---

# 9. fsck

## Purpose

Checks and repairs Linux filesystems.

### Syntax

```bash
sudo fsck /dev/sdb1
```

### Explanation

Used to detect and fix filesystem errors.

---

# 10. HDD vs SSD

## HDD (Hard Disk Drive)

- Mechanical storage device
- Uses spinning disks
- Slower
- Cheaper
- More storage capacity

---

## SSD (Solid State Drive)

- Flash memory
- No moving parts
- Faster
- More reliable
- Lower power consumption

---

## Difference

| HDD | SSD |
|------|------|
| Mechanical | Electronic |
| Slower | Faster |
| Cheaper | Expensive |
| More Power | Less Power |

---

# 11. Partition

## Purpose

A partition divides a physical disk into multiple logical sections.

### Example

```
512 GB SSD

├── C: Drive
├── D: Drive
└── E: Drive
```

### Linux Example

```
/dev/sda1
/dev/sda2
/dev/sda3
```

---

# 12. File System

A filesystem organizes how files are stored on storage devices.

## Common File Systems

| File System | Operating System |
|--------------|------------------|
| ext4 | Linux |
| XFS | Linux |
| NTFS | Windows |
| FAT32 | Windows / USB |
| exFAT | Windows, Linux, macOS |

---

# 13. Inode

## Purpose

An inode stores metadata about a file.

It contains

- File Size
- Owner
- Permissions
- Creation Time
- Modification Time

### Check Inode

```bash
ls -i
```

---

# Summary

| Command / Concept | Purpose |
|-------------------|----------|
| mount | Attach filesystem |
| umount | Detach filesystem |
| mkfs | Create filesystem |
| fsck | Check and repair filesystem |
| HDD | Mechanical storage |
| SSD | Flash storage |
| Partition | Divide disk |
| File System | Organize files |
| Inode | Stores file metadata |

---

# Interview Questions

### Q1. What is the purpose of mount?

It attaches a filesystem to a directory.

---

### Q2. Why should you unmount a device before removing it?

To avoid data corruption.

---

### Q3. Which command creates a filesystem?

```bash
mkfs
```

---

### Q4. Which command repairs a filesystem?

```bash
fsck
```

---

### Q5. Which Linux filesystem is most commonly used?

ext4

---

### Q6. Which command displays inode numbers?

```bash
ls -i
```

---

### Q7. What does an inode store?

File metadata such as permissions, owner, timestamps, and size.