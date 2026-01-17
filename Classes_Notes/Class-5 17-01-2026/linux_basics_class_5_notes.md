# Linux Basics – Class 5 (Deep Dive Notes)

**Program:** Multi-Cloud + DevSecOps  
**Class:** 5  
**Date:** 17 January 2026  
**Trainer:** Cloud Tech Hacks

---

## 1. What is Linux?

Linux is an **open-source operating system kernel**. A kernel is the core part of an operating system that directly communicates with the hardware and manages system resources.

Linux by itself is **not a complete operating system**. A complete Linux Operating System is built using:

- Linux Kernel
- System Libraries
- System Utilities
- User Interface (CLI / GUI)

When these components are combined, they form a **Linux Distribution (Distro)**.

---

## 2. Why Linux is Important in Cloud & DevOps

Linux is the backbone of modern IT infrastructure.

- Most cloud servers run on Linux
- Containers (Docker, Kubernetes) are Linux-based
- DevOps tools are primarily designed for Linux
- High performance, security, and stability

That is why Linux is a **mandatory skill** for Cloud, DevOps, and SRE roles.

---

## 3. Kernel – The Heart of Operating System

The Kernel acts as a bridge between **hardware** and **software**.

### Responsibilities of Kernel

- CPU Scheduling (which process runs and when)
- Memory (RAM) Management
- Process Management
- Device Management via Drivers
- File System Management
- Network Management

Without the kernel, the OS cannot function.

---

## 4. Hardware, Drivers & OS Relationship

Hardware components such as:

- CPU
- RAM
- Monitor
- Keyboard
- Mouse
- Printer
- Speaker

cannot directly communicate with applications.

**Device Drivers** act as translators between:

Hardware → Kernel → Operating System → Applications

Example:
- Dell Monitor → Monitor Driver → Kernel → OS Display Output

---

## 5. Linux-Based Operating Systems (Distributions)

Popular Linux Distributions include:

- Ubuntu (Server & Desktop)
- CentOS / Rocky Linux
- Red Hat Enterprise Linux (RHEL)
- Kali Linux (Security & Penetration Testing)
- Parrot OS (Security)
- Android (Mobile OS based on Linux Kernel)

Each distro uses the same Linux kernel but differs in tools, package managers, and UI.

---

## 6. Windows vs Linux – Detailed Comparison

| Feature | Windows | Linux |
|------|--------|-------|
| Source Code | Closed | Open Source |
| Cost | Paid License | Free / Paid (Enterprise) |
| Customization | Limited | Very High |
| Security | Moderate | High |
| Performance | Resource Heavy | Lightweight |
| Server Usage | Limited | Dominant |
| Cloud Usage | Low | Very High |

---

## 7. User Management Basics

### Check Logged-in User

**Windows:**
- Visible via Start Menu or Control Panel

**Linux:**
```bash
whoami
```

This command shows the current logged-in user.

---

## 8. Present Working Directory (PWD)

The Present Working Directory tells us **where we are currently located** in the file system.

**Windows:**
- Shown in File Explorer address bar

**Linux:**
```bash
pwd
```

---

## 9. Directory Navigation

### Move into a Directory
```bash
cd folder_name
```

### Move Back to Parent Directory
```bash
cd ..
```

### Move to Home Directory
```bash
cd ~
```

---

## 10. Listing Files and Directories

**Windows:**
- Double-click folder in File Explorer

**Linux:**
```bash
ls
ls -l
ls -a
```

- `ls` → List files
- `ls -l` → Detailed view
- `ls -a` → Hidden files

---

## 11. Linux File System Structure

Linux follows a **single-rooted directory structure**.

Important directories:

- `/` → Root directory
- `/home` → User home directories
- `/etc` → Configuration files
- `/var` → Logs and variable data
- `/bin` → Essential binaries
- `/usr` → User programs
- `/tmp` → Temporary files

Unlike Windows, Linux does not use drive letters.

---

## 12. File Editing in Linux

Linux provides multiple CLI-based text editors.

### Nano (Beginner Friendly)
```bash
nano file.txt
```

### Vim (Advanced)
```bash
vi file.txt
```

Used heavily for:
- Configuration files
- Server administration
- DevOps automation

---

## 13. Software Installation in Linux

Linux uses **package managers** instead of setup.exe files.

### Ubuntu / Debian
```bash
sudo apt update
sudo apt install nginx -y
```

### RedHat / CentOS
```bash
sudo yum install nginx -y
```

---

## 14. Process Management

A process is a running program.

### Windows
- Task Manager

### Linux
```bash
ps -ef
top
htop
```

- `ps -ef` → Snapshot of processes
- `top` → Live process monitoring

---

## 15. Everything is a File (Linux Philosophy)

In Linux:

- Regular files
- Directories
- Hardware devices
- Network sockets
- Processes

are all treated as files.

This design makes Linux powerful, consistent, and script-friendly.

---

## 16. Absolute vs Relative Path

### Absolute Path

- Starts from root `/`
- Full location of file

Example:
```bash
/home/cloudtechhacks/index.html
```

### Relative Path

- Based on current directory

Example:
```bash
./index.html
```

---

## 17. Final Lab Goal – Nginx Deployment Overview

### Objective
Deploy Starbucks Clone application on Nginx Web Server.

### High-Level Steps

- Install Nginx
- Clone GitHub repository
- Copy files to web root
- Start Nginx service
- Access application via browser

GitHub Repo:
https://github.com/jayp1993/Starbucks-Clone.git

---

## 18. Key Takeaways

- Linux is kernel-based OS
- Essential for Cloud & DevOps careers
- CLI-driven and automation-friendly
- Used extensively in servers and production environment