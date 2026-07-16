# File Permissions Commands

## 1. chmod (Change File Permissions)

### Purpose

The `chmod` command is used to change the permissions of files and directories.

### Syntax

```bash
chmod [permissions] filename
```

### Examples

Give execute permission to the owner

```bash
chmod u+x script.sh
```

Remove write permission from the group

```bash
chmod g-w file.txt
```

Give read permission to everyone

```bash
chmod a+r file.txt
```

Using numeric permissions

```bash
chmod 755 script.sh
```

```bash
chmod 644 notes.txt
```

### Common Numeric Permissions

| Permission | Meaning |
|------------|---------|
| 777 | Read, Write and Execute for everyone |
| 755 | Owner: Read, Write, Execute<br>Group: Read, Execute<br>Others: Read, Execute |
| 700 | Only owner has all permissions |
| 644 | Owner: Read, Write<br>Group: Read<br>Others: Read |

### Explanation

`chmod` is commonly used to control who can read, write, or execute a file or directory.

---

## 2. chown (Change File Owner)

### Purpose

The `chown` command changes the owner of a file or directory.

### Syntax

```bash
sudo chown owner filename
```

### Examples

Change owner

```bash
sudo chown himanshu notes.txt
```

Change owner and group

```bash
sudo chown himanshu:developers project.txt
```

Change ownership recursively

```bash
sudo chown -R himanshu Project/
```

### Explanation

`chown` is mainly used by the root user or administrator to transfer ownership of files and directories.

---

## 3. chgrp (Change Group Ownership)

### Purpose

The `chgrp` command changes the group ownership of a file or directory.

### Syntax

```bash
sudo chgrp group_name filename
```

### Example

```bash
sudo chgrp developers notes.txt
```

Change group recursively

```bash
sudo chgrp -R developers Project/
```

### Explanation

`chgrp` is useful when multiple users in the same group need access to shared files.

---

## 4. umask

### Purpose

The `umask` command sets the default permissions for newly created files and directories.

### Syntax

```bash
umask
```

Display symbolic format

```bash
umask -S
```

Set a new umask value

```bash
umask 022
```

### Example

```bash
umask
```

### Sample Output

```
0022
```

### Explanation

A `umask` value of `022` means:

- New files → 644
- New directories → 755

The umask removes permissions from the default values.

---

# Understanding Linux File Permissions

Every file has three types of users:

- Owner (u)
- Group (g)
- Others (o)

Permission Types:

| Symbol | Meaning |
|--------|---------|
| r | Read |
| w | Write |
| x | Execute |

Example:

```text
-rwxr-xr--
```

Breakdown:

| Section | Meaning |
|---------|---------|
| rwx | Owner has Read, Write, Execute |
| r-x | Group has Read and Execute |
| r-- | Others have Read only |

---

# Useful Commands

Check file permissions

```bash
ls -l
```

Example Output

```text
-rwxr-xr-x 1 himanshu developers 1200 Jul 15 script.sh
```

---

# Summary

| Command | Purpose |
|----------|---------|
| chmod | Change file permissions |
| chown | Change file owner |
| chgrp | Change group ownership |
| umask | Set default permissions for new files and directories |
| ls -l | Display file permissions |

---

# Interview Tips

### Difference between chmod, chown and chgrp

| Command | Purpose |
|----------|---------|
| chmod | Changes file permissions |
| chown | Changes the file owner |
| chgrp | Changes the file's group |

### Common Interview Questions

**Q1. What does chmod 755 mean?**

- Owner: Read, Write, Execute
- Group: Read, Execute
- Others: Read, Execute

**Q2. What does chmod 644 mean?**

- Owner: Read, Write
- Group: Read
- Others: Read

**Q3. Which command is used to check file permissions?**

```bash
ls -l
```