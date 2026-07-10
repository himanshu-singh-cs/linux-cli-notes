# File Management Commands

## 1. pwd (Print Working Directory)

### Purpose
Displays the current working directory.

### Syntax
```bash
pwd
```

### Example
```bash
pwd
```

### Output
```
/home/himanshu/Documents
```

---

## 2. ls (List Directory Contents)

### Purpose
Lists files and directories.

### Syntax
```bash
ls
```

### Common Options

```bash
ls -l
```
Shows detailed information.

```bash
ls -a
```
Shows hidden files.

```bash
ls -la
```
Shows hidden files with detailed information.

---

## 3. cd (Change Directory)

### Purpose
Changes the current directory.

### Syntax
```bash
cd folder_name
```

### Examples

```bash
cd Documents
```

```bash
cd ..
```

```bash
cd ~
```

---

## 4. mkdir (Make Directory)

### Purpose
Creates a new directory.

### Syntax

```bash
mkdir folder_name
```

### Example

```bash
mkdir DevOps
```

---

## 5. touch

### Purpose
Creates an empty file.

### Syntax

```bash
touch filename
```

### Example

```bash
touch notes.txt
```

---

## 6. cp (Copy Files)

### Syntax

```bash
cp source destination
```

### Example

```bash
cp file.txt backup.txt
```

---

## 7. mv (Move/Rename Files)

### Syntax

```bash
mv source destination
```

### Example

```bash
mv old.txt new.txt
```

---

## 8. rm (Remove Files)

### Syntax

```bash
rm filename
```

### Examples

```bash
rm file.txt
```

```bash
rm -r folder
```

```bash
rm -rf folder
```

---

## 9. cat

### Purpose
Displays file contents.

```bash
cat filename
```

---

## 10. head

Shows the first 10 lines of a file.

```bash
head filename
```

---

## 11. tail

Shows the last 10 lines of a file.

```bash
tail filename
```
---

## 12. rmdir (Remove Empty Directory)

### Purpose
Removes an empty directory.

### Syntax

```bash
rmdir directory_name
```

### Example

```bash
rmdir TestFolder
```

### Note

- Removes only **empty directories**.
- If the directory contains files or subdirectories, `rmdir` will fail.
- To remove a non-empty directory, use `rm -r`.

---

## 13. less

### Purpose

Displays the contents of a file one screen at a time. It allows both forward and backward navigation.

### Syntax

```bash
less filename
```

### Example

```bash
less notes.txt
```

### Useful Keys

| Key | Action |
|------|--------|
| ↑ / ↓ | Scroll line by line |
| Space | Next page |
| b | Previous page |
| /word | Search for a word |
| q | Quit |

### Why use `less`?

- Best for reading large files.
- Does not load the entire file into memory.
- Allows searching and scrolling in both directions.

---

## 14. more

### Purpose

Displays file contents one page at a time.

### Syntax

```bash
more filename
```

### Example

```bash
more notes.txt
```

### Useful Keys

| Key | Action |
|------|--------|
| Space | Next page |
| Enter | Next line |
| q | Quit |

### Difference between `less` and `more`

| less | more |
|------|------|
| Forward and backward navigation | Mostly forward navigation |
| Search supported | Limited search |
| More powerful | Simpler command |
| Preferred for large files | Suitable for basic viewing |