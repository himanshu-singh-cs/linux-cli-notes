# Process Management Commands

## 1. ps (Process Status)

### Purpose

Displays information about currently running processes.

### Syntax

```bash
ps
```

### Common Options

Show all running processes

```bash
ps -e
```

Detailed information

```bash
ps -ef
```

Show processes for current user

```bash
ps -u
```

### Example

```bash
ps -ef
```

### Explanation

The `ps` command provides a snapshot of running processes.

---

## 2. top

### Purpose

Displays running processes in real time.

### Syntax

```bash
top
```

### Features

- CPU Usage
- Memory Usage
- Running Processes
- Load Average
- Process IDs

### Exit

Press

```text
q
```

---

## 3. kill

### Purpose

Terminates a process using its Process ID (PID).

### Syntax

```bash
kill PID
```

### Example

```bash
kill 2456
```

Force kill

```bash
kill -9 2456
```

### Explanation

`kill -9` forcefully stops a process.

---

## 4. killall

### Purpose

Kills all processes having the same name.

### Syntax

```bash
killall process_name
```

### Example

```bash
killall firefox
```

---

## 5. jobs

### Purpose

Displays background jobs running in the current shell.

### Syntax

```bash
jobs
```

### Example

```bash
jobs
```

---

## 6. bg (Background)

### Purpose

Continues a stopped process in the background.

### Syntax

```bash
bg %job_number
```

### Example

```bash
bg %1
```

---

## 7. fg (Foreground)

### Purpose

Brings a background process to the foreground.

### Syntax

```bash
fg %job_number
```

### Example

```bash
fg %1
```

---

## 8. nice

### Purpose

Starts a process with a specific priority.

### Syntax

```bash
nice -n priority command
```

### Example

```bash
nice -n 10 python app.py
```

---

## 9. renice

### Purpose

Changes the priority of an already running process.

### Syntax

```bash
renice priority PID
```

### Example

```bash
sudo renice 5 2456
```

---

## 10. uptime

### Purpose

Shows how long the system has been running.

### Syntax

```bash
uptime
```

### Sample Output

```text
10:45:20 up 5 days, 4:10, 2 users, load average: 0.20, 0.35, 0.40
```

---

# Understanding Process States

| State | Meaning |
|--------|---------|
| Running | Process is currently executing |
| Sleeping | Waiting for an event |
| Stopped | Process has been paused |
| Zombie | Process has finished but entry still exists |

---

# Useful Commands

Current shell PID

```bash
echo $$
```

Find process by name

```bash
pgrep nginx
```

View process tree

```bash
pstree
```

---

# Summary

| Command | Purpose |
|----------|---------|
| ps | Show running processes |
| top | Real-time process monitor |
| kill | Kill process using PID |
| killall | Kill processes by name |
| jobs | Show background jobs |
| bg | Run process in background |
| fg | Bring process to foreground |
| nice | Start process with priority |
| renice | Change running process priority |
| uptime | Show system uptime |

# Interview Tips

## Difference between kill and killall

| kill | killall |
|------|----------|
| Uses PID | Uses process name |

---

## Difference between ps and top

| ps | top |
|----|-----|
| Snapshot | Live monitoring |

---

## Common Interview Questions

### Q1. Which command shows real-time running processes?

```bash
top
```

### Q2. Which command forcefully kills a process?

```bash
kill -9 PID
```

### Q3. Which command shows system uptime?

```bash
uptime
```

### Q4. How do you display all running processes?

```bash
ps -ef
```