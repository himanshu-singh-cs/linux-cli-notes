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

---

---

# 6. sed (Stream Editor)

## Purpose

The `sed` command is used to search, replace, insert, and delete text in a file.

### Syntax

```bash
sed 'operation' filename
```

### Examples

Replace "Linux" with "Ubuntu"

```bash
sed 's/Linux/Ubuntu/' notes.txt
```

Replace all occurrences

```bash
sed 's/Linux/Ubuntu/g' notes.txt
```

Display specific line

```bash
sed -n '5p' notes.txt
```

### Explanation

`sed` is commonly used for text replacement and editing files without opening them.

---

# 7. awk

## Purpose

The `awk` command is used for pattern scanning and processing text.

### Syntax

```bash
awk '{print}' filename
```

### Examples

Print first column

```bash
awk '{print $1}' data.txt
```

Print second column

```bash
awk '{print $2}' data.txt
```

Print line number and content

```bash
awk '{print NR, $0}' data.txt
```

### Explanation

`awk` is powerful for processing structured text and reports.

---

# 8. wc (Word Count)

## Purpose

Counts lines, words, and characters.

### Syntax

```bash
wc filename
```

### Examples

Count lines

```bash
wc -l notes.txt
```

Count words

```bash
wc -w notes.txt
```

Count characters

```bash
wc -m notes.txt
```

---

# 9. cut

## Purpose

Extracts specific columns from a file.

### Syntax

```bash
cut options filename
```

### Examples

Extract first field

```bash
cut -d',' -f1 students.csv
```

Extract second field

```bash
cut -d':' -f2 /etc/passwd
```

---

# 10. head

## Purpose

Displays the first lines of a file.

### Syntax

```bash
head filename
```

### Examples

First 10 lines

```bash
head notes.txt
```

First 5 lines

```bash
head -5 notes.txt
```

---

# 11. tail

## Purpose

Displays the last lines of a file.

### Syntax

```bash
tail filename
```

### Examples

Last 10 lines

```bash
tail notes.txt
```

Last 20 lines

```bash
tail -20 notes.txt
```

Follow log file

```bash
tail -f /var/log/syslog
```

### Explanation

`tail -f` is useful for monitoring log files in real time.

---

# Summary

| Command | Purpose |
|----------|----------|
| sed | Edit and replace text |
| awk | Process text by fields |
| wc | Count lines, words, characters |
| cut | Extract specific columns |
| head | Display first lines |
| tail | Display last lines |

---

# Interview Questions

### Q1. Which command is used to replace text in a file?

```bash
sed
```

---

### Q2. Which command is used to process columns?

```bash
awk
```

---

### Q3. Which command counts words?

```bash
wc -w
```

---

### Q4. Which command displays the first 10 lines?

```bash
head
```

---

### Q5. Which command monitors a log file in real time?

```bash
tail -f
```

---

---

# 12. tee

## Purpose

The `tee` command displays command output on the terminal and also writes it to a file.

### Syntax

```bash
command | tee filename
```

### Examples

Save output to a file

```bash
ls -l | tee files.txt
```

Append output

```bash
ls -l | tee -a files.txt
```

### Explanation

`tee` is useful when you want to view the output and save it at the same time.

---

# 13. diff

## Purpose

The `diff` command compares two files line by line.

### Syntax

```bash
diff file1 file2
```

### Example

```bash
diff old.txt new.txt
```

### Explanation

It shows the differences between two files.

---

# 14. xargs

## Purpose

The `xargs` command converts input into command-line arguments.

### Syntax

```bash
command | xargs another_command
```

### Examples

Delete multiple files

```bash
find . -name "*.log" | xargs rm
```

Count lines in multiple files

```bash
find . -name "*.txt" | xargs wc -l
```

### Explanation

`xargs` is commonly used with `find`, `grep`, and `cat` to process multiple files efficiently.

---

# Real World DevOps Examples

## Search "error" in application logs

```bash
grep "ERROR" app.log
```

---

## Monitor logs in real time

```bash
tail -f /var/log/syslog
```

---

## Find Docker files

```bash
find . -name "Dockerfile"
```

---

## Count log lines

```bash
wc -l app.log
```

---

## Replace text inside configuration file

```bash
sed 's/http/https/g' config.conf
```

---

## Display first column from CSV

```bash
awk -F',' '{print $1}' employees.csv
```

---

## Save command output and display it

```bash
ls -lh | tee output.txt
```

---

# Common Mistakes

❌ Using `uniq` without `sort`

Correct

```bash
sort names.txt | uniq
```

---

❌ Forgetting `-f` while monitoring logs

Correct

```bash
tail -f app.log
```

---

❌ Running `find` from the wrong directory

Correct

```bash
find /home -name "*.txt"
```

---

# Summary

| Command | Purpose |
|----------|----------|
| grep | Search text |
| find | Search files |
| locate | Fast file search |
| sort | Sort data |
| uniq | Remove duplicates |
| sed | Replace/edit text |
| awk | Process structured text |
| wc | Count lines, words, characters |
| cut | Extract columns |
| head | Display first lines |
| tail | Display last lines |
| tee | Save and display output |
| diff | Compare files |
| xargs | Pass input as arguments |

---

# Interview Questions

### Q1. Which command compares two files?

```bash
diff
```

---

### Q2. Which command writes output to both terminal and a file?

```bash
tee
```

---

### Q3. Which command passes output as arguments to another command?

```bash
xargs
```

---

### Q4. Which command monitors logs continuously?

```bash
tail -f
```

---

### Q5. Which command is used to search text inside a file?

```bash
grep
```

---

### Q6. Which command searches files based on name?

```bash
find
```

---

### Q7. Which command is faster for searching files?

```bash
locate
```