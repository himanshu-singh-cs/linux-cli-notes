# Archive and Compression Commands

## What is Archiving?

Archiving means combining multiple files and directories into a single file.

Example:

```
Documents
Photos
Videos
```

↓

```
backup.tar
```

**Note:** Archiving does **not** reduce file size.

---

# What is Compression?

Compression reduces the size of files to save storage space and make file transfer faster.

Example:

```
backup.tar
```

↓

```
backup.tar.gz
```

---

# 1. tar (Tape Archive)

## Purpose

The `tar` command is used to archive multiple files and directories into a single file.

### Syntax

```bash
tar [options] archive_name files
```

### Create archive

```bash
tar -cvf backup.tar Documents/
```

### Extract archive

```bash
tar -xvf backup.tar
```

### List archive contents

```bash
tar -tvf backup.tar
```

### Explanation

- `-c` → Create archive
- `-x` → Extract archive
- `-v` → Verbose output
- `-f` → Specify archive filename
- `-t` → List archive contents

---

# 2. gzip

## Purpose

Compresses a file.

### Syntax

```bash
gzip filename
```

### Example

```bash
gzip backup.tar
```

Output

```
backup.tar.gz
```

### Explanation

The original file is replaced with the compressed file.

---

# 3. gunzip

## Purpose

Decompresses a `.gz` file.

### Syntax

```bash
gunzip filename.gz
```

### Example

```bash
gunzip backup.tar.gz
```

---

# 4. tar with gzip

### Create compressed archive

```bash
tar -czvf backup.tar.gz Documents/
```

### Extract compressed archive

```bash
tar -xzvf backup.tar.gz
```

### Explanation

This combines archiving and compression into one command.

---

# Summary

| Command | Purpose |
|----------|----------|
| tar | Create or extract archives |
| gzip | Compress files |
| gunzip | Decompress files |
| tar -czvf | Create compressed archive |
| tar -xzvf | Extract compressed archive |

---

# Interview Questions

### Q1. What is the difference between archiving and compression?

| Archiving | Compression |
|------------|-------------|
| Combines files | Reduces file size |

---

### Q2. Which command creates a tar archive?

```bash
tar -cvf
```

---

### Q3. Which command extracts a tar archive?

```bash
tar -xvf
```

---

### Q4. Which command compresses a file?

```bash
gzip
```

---

### Q5. Which command decompresses a .gz file?

```bash
gunzip
```