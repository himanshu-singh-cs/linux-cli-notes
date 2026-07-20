# Package Management Commands

## What is Package Management?

Package management is the process of installing, updating, removing, and managing software on a Linux system.

A package manager automatically handles software installation along with its dependencies.

---

# 1. apt (Advanced Package Tool)

## Purpose

The `apt` command is used to install, update, remove, and manage software packages on Debian and Ubuntu based Linux systems.

### Syntax

```bash
apt [command] package_name
```

### Examples

Update package list

```bash
sudo apt update
```

Upgrade installed packages

```bash
sudo apt upgrade
```

Install a package

```bash
sudo apt install nginx
```

Remove a package

```bash
sudo apt remove nginx
```

Remove package along with configuration files

```bash
sudo apt purge nginx
```

Search a package

```bash
apt search docker
```

Show package information

```bash
apt show nginx
```

List installed packages

```bash
apt list --installed
```

### Explanation

`apt` is the most commonly used package manager in Ubuntu and Debian.

---

# 2. apt-get

## Purpose

`apt-get` is the older package management tool.

It is mostly used in automation scripts.

### Examples

```bash
sudo apt-get update
```

```bash
sudo apt-get upgrade
```

```bash
sudo apt-get install git
```

### Difference between apt and apt-get

| apt | apt-get |
|------|----------|
| User-friendly | Script-friendly |
| Better output | Older tool |
| Used daily | Used in automation |

---

# 3. dpkg

## Purpose

Installs or manages local `.deb` packages.

### Install a package

```bash
sudo dpkg -i package.deb
```

### Remove package

```bash
sudo dpkg -r package_name
```

### List installed packages

```bash
dpkg -l
```

### Explanation

Unlike `apt`, `dpkg` does not automatically install dependencies.

---

# Summary

| Command | Purpose |
|----------|----------|
| apt | Install and manage packages |
| apt-get | Package management (older tool) |
| dpkg | Install local .deb packages |

---

# Interview Questions

### Q1. Which package manager is used in Ubuntu?

```bash
apt
```

---

### Q2. Which command updates the package list?

```bash
sudo apt update
```

---

### Q3. Which command upgrades installed packages?

```bash
sudo apt upgrade
```

---

### Q4. Which command installs a local .deb package?

```bash
sudo dpkg -i package.deb
```

---

### Q5. Difference between apt and dpkg?

| apt | dpkg |
|------|------|
| Installs packages with dependencies | Installs local .deb packages |
| Downloads from repositories | Works on local package files |

---

# 4. yum (Yellowdog Updater Modified)

## Purpose

`yum` is a package manager used in older Red Hat, CentOS, and RHEL systems.

### Examples

Update packages

```bash
sudo yum update
```

Install a package

```bash
sudo yum install nginx
```

Remove a package

```bash
sudo yum remove nginx
```

Search for a package

```bash
yum search docker
```

### Explanation

`yum` automatically resolves package dependencies during installation.

---

# 5. dnf (Dandified YUM)

## Purpose

`dnf` is the modern replacement for `yum`.

It is used in Fedora, RHEL 8+, Rocky Linux, and AlmaLinux.

### Examples

Install a package

```bash
sudo dnf install git
```

Update packages

```bash
sudo dnf update
```

Remove a package

```bash
sudo dnf remove git
```

### Difference between yum and dnf

| yum | dnf |
|------|------|
| Older package manager | Modern package manager |
| Slower | Faster |
| More memory usage | Better dependency resolution |

---

# 6. rpm (RPM Package Manager)

## Purpose

`rpm` is used to install and manage local `.rpm` packages.

### Install package

```bash
sudo rpm -ivh package.rpm
```

### Remove package

```bash
sudo rpm -e package_name
```

### Display installed packages

```bash
rpm -qa
```

### Explanation

Unlike `yum` or `dnf`, `rpm` does not automatically resolve dependencies.

---

# 7. snap

## Purpose

`snap` installs applications with all required dependencies bundled together.

### Install package

```bash
sudo snap install code --classic
```

### List installed packages

```bash
snap list
```

### Remove package

```bash
sudo snap remove code
```

---

# 8. flatpak

## Purpose

Flatpak is another package management system for distributing desktop applications.

### Install package

```bash
flatpak install flathub org.videolan.VLC
```

### List packages

```bash
flatpak list
```

### Remove package

```bash
flatpak uninstall org.videolan.VLC
```

---

# 9. Repository (Repo)

## Purpose

A repository is an online storage location that contains software packages.

Examples

- Ubuntu Repository
- Debian Repository
- Fedora Repository

When you run

```bash
sudo apt install nginx
```

the package is downloaded from a repository.

---

# 10. Dependency

## Purpose

A dependency is another package required for a program to work correctly.

### Example

Docker may require several libraries.

When you install Docker using

```bash
sudo apt install docker.io
```

`apt` automatically installs all required dependencies.

---

# Real World DevOps Examples

Update package list

```bash
sudo apt update
```

Install Git

```bash
sudo apt install git
```

Install Nginx

```bash
sudo apt install nginx
```

Install Docker

```bash
sudo apt install docker.io
```

Install Java

```bash
sudo apt install openjdk-17-jdk
```

---

# Common Mistakes

❌ Forgetting to update package list

Wrong

```bash
sudo apt install nginx
```

Correct

```bash
sudo apt update
sudo apt install nginx
```

---

❌ Using rpm without dependencies

Better option

```bash
sudo dnf install package.rpm
```

---

# Summary

| Command | Purpose |
|----------|----------|
| apt | Debian/Ubuntu package manager |
| apt-get | Older package manager |
| dpkg | Install local .deb packages |
| yum | Older RHEL package manager |
| dnf | Modern RHEL package manager |
| rpm | Install local .rpm packages |
| snap | Universal package manager |
| flatpak | Cross-platform package manager |

---

# Interview Questions

### Q1. Which package manager is used in Ubuntu?

apt

---

### Q2. Which package manager replaced yum?

dnf

---

### Q3. Which command installs local .rpm packages?

```bash
rpm -ivh package.rpm
```

---

### Q4. Which package manager installs local .deb packages?

```bash
dpkg
```

---

### Q5. What is a repository?

A repository is an online storage location that contains software packages.

---

### Q6. What is a dependency?

A dependency is a package required by another package to work properly.

---

### Q7. Difference between rpm and dpkg?

| rpm | dpkg |
|------|------|
| Used in RHEL/CentOS | Used in Debian/Ubuntu |
| Works with .rpm files | Works with .deb files |

---

### Q8. Difference between apt and yum?

| apt | yum |
|------|------|
| Debian/Ubuntu | RHEL/CentOS |