# Linux Fundamentals and File System

## Main Idea
This chapter introduces the Linux operating system structure, focusing on the
Linux file system, basic commands, users and groups, permissions, and essential
system concepts used in daily administration and security operations.

---

## Linux File System Structure
Linux uses a hierarchical file system that starts from the root directory (/).

- **/** Root of the file system
- **/root** Home directory of the root user
- **/home** Home directories for regular users
- **/bin** Essential binary executables
- **/sbin** System binaries for administrative tasks
- **/etc** System configuration files
- **/var** Variable data (logs, cache, spool files)
- **/dev** Device files
- **/proc** Virtual file system for processes and system info
- **/tmp** Temporary files
- **/usr** User utilities and shared libraries
- **/opt** Optional third-party software
- **/boot** Boot loader and kernel files

---

## Default Shell
The default shell for most Linux users is **Bash**.
- `$` indicates a normal user
- `#` indicates the root user

---

## File and Directory Management Commands
Common commands used to navigate and manage files and directories:

- `ls` – list directory contents
- `cd` – change directory
- `pwd` – display current directory path
- `mkdir` – create a directory
- `rmdir` – remove an empty directory
- `cp` – copy files or directories
- `mv` – move or rename files and directories
- `touch` – create an empty file
- `find` – search for files and directories
- `su` – switch user

---

## File Viewing and Editing
Commands used to view and edit file contents:

- `cat` – display file contents
- `less` / `more` – view files page by page
- `head` – display first lines of a file
- `tail` – display last lines of a file
- `nano` – simple text editor
- `vim` – advanced text editor

---

## System Information Commands
Commands used to monitor system status:

- `uname` – system information
- `top` / `htop` – real-time process monitoring
- `df` – disk space usage
- `free` – memory usage
- `uptime` – system running time

---

## User Management
Linux uses user accounts to control access.

- `who` – show logged-in users
- `whoami` – display current user
- `adduser` – create a new user (requires sudo)
- `deluser` – remove a user (requires sudo)
- `passwd` – change user password

---

## File Types
- **Regular files:** text, images, data files
- **Executable files:** scripts or binaries
- **Special files:** device files

---

## File Permissions
Linux permissions define access control:

- **r** – read
- **w** – write
- **x** – execute

Numeric representation:
- read = 4
- write = 2
- execute = 1

Permission scope:
- **u** – user (owner)
- **g** – group
- **o** – others
- **a** – all

---

## Ownership and Permissions Management
- `chmod` – change file or directory permissions
- `chown` – change file or directory ownership

---

## Compression and Archiving

### Compression Tools
- `gzip` (.gz)
- `bzip2` (.bz2)
- `xz` (.xz)

Using `-c` keeps the original file.

### Tar Archives
- `c` – create archive
- `x` – extract archive
- `t` – list archive contents
- `z` – gzip compression
- `j` – bzip2 compression
- `v` – verbose output
- `f` – specify archive name

---

## Users and Groups
Linux supports three main account types:

- **Root user:** UID 0
- **System users:** UID 1–999
- **Regular users:** UID 1000+

Group management:
- `groupadd` – create a group
- `usermod -g` – add user to a group
- `gpasswd -d` – remove user from a group

---

## Networking Basics
Basic networking commands:

- `ping` – test network connectivity
- `ifconfig` – display network interfaces
- `ip` – manage network interfaces and routing
- `netstat` – display network connections
- `curl` – transfer data to/from servers

---

## Security Perspective
Understanding Linux fundamentals is critical for cybersecurity because
misconfigured permissions, weak user management, and insecure services
can lead to unauthorized access and system compromise.
