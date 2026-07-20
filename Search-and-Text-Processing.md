# Search and Text Processing Commands

## 1. grep (Global Regular Expression Print)

### Purpose

The `grep` command searches for a specific word or pattern inside a file.

### Syntax

```bash
grep "pattern" filename
```

### Examples

Search the word "error"

```bash
grep "error" log.txt
```

Ignore case

```bash
grep -i "linux" notes.txt
```

Show line numbers

```bash
grep -n "main" Hello.java
```

Search recursively

```bash
grep -r "docker" Project/
```

### Explanation

`grep` is commonly used to search logs, configuration files, and source code.

---

## 2. find

### Purpose

The `find` command searches for files and directories.

### Syntax

```bash
find path options
```

### Examples

Find a file

```bash
find . -name "notes.txt"
```

Find all shell scripts

```bash
find . -name "*.sh"
```

Find directories

```bash
find . -type d
```

Find files larger than 100 MB

```bash
find . -size +100M
```

### Explanation

`find` searches files based on name, size, type, permissions, and many other conditions.

---

## 3. locate

### Purpose

Find files quickly using a prebuilt database.

### Syntax

```bash
locate filename
```

### Example

```bash
locate passwd
```

### Update Database

```bash
sudo updatedb
```

### Explanation

`locate` is much faster than `find`, but it depends on an updated database.

---

## 4. sort

### Purpose

Sorts lines alphabetically or numerically.

### Syntax

```bash
sort filename
```

### Examples

Alphabetical order

```bash
sort names.txt
```

Reverse order

```bash
sort -r names.txt
```

Numeric sorting

```bash
sort -n numbers.txt
```

---

## 5. uniq

### Purpose

Removes duplicate consecutive lines.

### Syntax

```bash
uniq filename
```

### Example

```bash
sort names.txt | uniq
```

Count duplicate lines

```bash
uniq -c names.txt
```

### Explanation

`uniq` works best with sorted input.

---

## Summary

| Command | Purpose |
|----------|---------|
| grep | Search text inside files |
| find | Search files and directories |
| locate | Quickly find files |
| sort | Sort lines |
| uniq | Remove duplicate lines |

---

# Interview Questions

### Q1. Difference between grep and find?

| grep | find |
|------|------|
| Searches inside files | Searches files/directories |

---

### Q2. Which command searches files faster?

```bash
locate
```

---

### Q3. Which command removes duplicate lines?

```bash
uniq
```

---

### Q4. Which command sorts text?

```bash
sort
```