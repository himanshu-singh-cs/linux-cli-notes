# User Management Commands

## 1. whoami

### Purpose
Displays the username of the currently logged-in user.

### Syntax

```bash
whoami
```

### Example

```bash
whoami
```

### Output

```
himanshu
```

---

## 2. id

### Purpose
Displays user ID (UID), group ID (GID), and group memberships.

### Syntax

```bash
id
```

### Example

```bash
id
```

### Sample Output

```
uid=1000(himanshu) gid=1000(himanshu) groups=1000(himanshu)
```

---

## 3. passwd

### Purpose
Changes the password of the current user.

### Syntax

```bash
passwd
```

### Change another user's password (root)

```bash
sudo passwd username
```

### Example

```bash
passwd
```

---

## 4. useradd

### Purpose
Creates a new user account.

### Syntax

```bash
sudo useradd username
```

### Example

```bash
sudo useradd devops
```

### Verify User

```bash
id devops
```

---

## 5. usermod

### Purpose
Modifies an existing user account.

### Syntax

```bash
sudo usermod [options] username
```

### Example

Add user to sudo group

```bash
sudo usermod -aG sudo devops
```

---

## 6. userdel

### Purpose
Deletes a user account.

### Syntax

```bash
sudo userdel username
```

### Delete user with home directory

```bash
sudo userdel -r username
```

### Example

```bash
sudo userdel devops
```

---

## 7. groups

### Purpose
Displays the groups a user belongs to.

### Syntax

```bash
groups
```

### Example

```bash
groups
```

### Sample Output

```
himanshu sudo docker
```

---

# Summary

| Command | Purpose |
|----------|---------|
| whoami | Display current username |
| id | Show user and group IDs |
| passwd | Change user password |
| useradd | Create a new user |
| usermod | Modify user account |
| userdel | Delete user account |
| groups | Show user groups |