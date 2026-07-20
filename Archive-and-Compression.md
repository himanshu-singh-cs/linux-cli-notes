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

---

---

# 5. zip

## Purpose

The `zip` command compresses one or more files into a `.zip` archive.

### Syntax

```bash
zip archive_name.zip files
```

### Examples

Compress a single file

```bash
zip notes.zip notes.txt
```

Compress multiple files

```bash
zip project.zip file1.txt file2.txt
```

Compress an entire directory

```bash
zip -r backup.zip Documents/
```

### Explanation

The `-r` option recursively compresses all files and subdirectories.

---

# 6. unzip

## Purpose

The `unzip` command extracts files from a `.zip` archive.

### Syntax

```bash
unzip archive.zip
```

### Examples

Extract archive

```bash
unzip backup.zip
```

Extract to a specific directory

```bash
unzip backup.zip -d /home/user/Documents
```

---

# 7. bzip2

## Purpose

Compresses files with a higher compression ratio than gzip.

### Syntax

```bash
bzip2 filename
```

### Example

```bash
bzip2 notes.txt
```

Output

```
notes.txt.bz2
```

---

# 8. bunzip2

## Purpose

Decompresses `.bz2` files.

### Syntax

```bash
bunzip2 filename.bz2
```

### Example

```bash
bunzip2 notes.txt.bz2
```

---

# 9. xz

## Purpose

Compresses files with an even higher compression ratio.

### Syntax

```bash
xz filename
```

### Example

```bash
xz notes.txt
```

Output

```
notes.txt.xz
```

---

# 10. unxz

## Purpose

Decompresses `.xz` files.

### Syntax

```bash
unxz filename.xz
```

### Example

```bash
unxz notes.txt.xz
```

---

# Difference between tar and zip

| tar | zip |
|------|-----|
| Mainly used in Linux | Used on Linux, Windows and macOS |
| Creates archive | Compresses into ZIP format |
| Often combined with gzip | Compression built-in |

---

# Common Compression Formats

| Extension | Tool |
|-----------|------|
| .tar | tar |
| .tar.gz | tar + gzip |
| .zip | zip |
| .bz2 | bzip2 |
| .xz | xz |

---

# Real World DevOps Examples

Create a backup

```bash
tar -czvf backup.tar.gz /var/www
```

Compress logs

```bash
gzip app.log
```

Extract a deployment package

```bash
tar -xzvf release.tar.gz
```

Compress project folder

```bash
zip -r project.zip Project/
```

---

# Common Mistakes

❌ Forgetting `-r` while compressing directories

Wrong

```bash
zip backup.zip Documents
```

Correct

```bash
zip -r backup.zip Documents
```

---

❌ Trying to extract `.tar.gz` using only `gunzip`

Correct

```bash
tar -xzvf backup.tar.gz
```

---

# Summary

| Command | Purpose |
|----------|----------|
| tar | Archive files |
| gzip | Compress files |
| gunzip | Decompress .gz files |
| zip | Create ZIP archive |
| unzip | Extract ZIP archive |
| bzip2 | High compression |
| bunzip2 | Decompress .bz2 |
| xz | Very high compression |
| unxz | Decompress .xz |

---

# Interview Questions

### Q1. Which command creates a ZIP archive?

```bash
zip
```

---

### Q2. Which command extracts a ZIP archive?

```bash
unzip
```

---

### Q3. Which command creates a compressed tar archive?

```bash
tar -czvf
```

---

### Q4. Which command extracts a `.tar.gz` archive?

```bash
tar -xzvf
```

---

### Q5. Which command compresses files into `.bz2` format?

```bash
bzip2
```

---

### Q6. Which command compresses files into `.xz` format?

```bash
xz
```

---

### Q7. Difference between `gzip` and `zip`?

| gzip | zip |
|-------|-----|
| Compresses a single file | Can compress multiple files/directories |
| Creates `.gz` file | Creates `.zip` archive |