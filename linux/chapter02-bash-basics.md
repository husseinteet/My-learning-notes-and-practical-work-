
# Chapter 2 – Bash & Linux Basics

## Bash
- A specific type of **shell**
- One of the most popular **Command Line Interfaces (CLI)**

## Shell
- A command-line interface that allows users to interact with the operating system
- Acts as a bridge between the **user** and the **system**

## Command Line
- A direct input interface used to execute commands

---

## Subshell
- A separate instance of the shell
- Created by enclosing commands inside parentheses `()`

### Subshell Use Cases
- Grouping commands
- Running multiple commands without affecting the parent shell
- Running background jobs

### Example: Grouping Commands
```bash
{
  echo "Starting process..."
  date
  echo "Process complete."
} > output.txt
````

---

## Command Substitution

* Allows the output of a command to be used as input for another command
* Methods:

  * Backticks `` `command` ``
  * `$()` (recommended)

### Using Backticks

```bash
current_date=`date`
echo "Today's date is: $current_date"
```

### Using `$()`

```bash
current_date=$(date)
echo "Today's date is: $current_date"
```

### Examples

```bash
echo "Current user: $(whoami)"
echo "Current directory: $(pwd)"
echo "Current shell: $(basename $SHELL)"
```

---

## Creating a Backup with Timestamp

```bash
cp myfile.txt "myfile_backup_$(date +'%y%m%d_%H%M%S').txt"
```

---

## Pipes and Redirection

### Pipes

* Allow the output of one command to be used as input to another command

### Output Redirection

* Overwrite output using `>`

```bash
ls -l > info.txt
```

* Append output using `>>`

```bash
ls -l >> info.txt
```

* Redirect errors using `2>`

```bash
abc 2> errorfile.txt
```

---

## Wildcards

* `*` → Matches everything
* `?` → Matches exactly one character
* `[ ]` → Matches any one character in a range
* `[!]` → Negation (not in the range)

---

## Aliases and Functions

### Aliases

* Shortcuts for longer commands

```bash
alias abc='ls -la'
```

### Functions

* More powerful and flexible than aliases

```bash
mkcd () {
  mkdir -p "$1" && cd "$1"
}
```

### List All Functions

```bash
declare -f
```

---

## Backup Function Example

```bash
backup-txt () {
  if [ -z "$1" ]; then
    echo "Usage: backup-txt <backup_name>"
    return 1
  fi

  tar -czvf "$1.tar.gz" *.txt
  echo "Backup created: $1.tar.gz"
}
```

---

## System Monitoring & Processes

### top

* Monitor system performance in real time

### Process States

* **Running**: Executing on the CPU
* **Sleeping**: Waiting for an event
* **Stopped**: Temporarily halted
* **Zombie**: Finished execution but still exists in the process table

### Process Management Commands

* `ps` → Display running processes
* `kill` → Terminate a process
* `pkill -KILL -u user` → Terminate all processes for a user

---

## System Information Commands

* `w` → Show logged-in users
* `uptime` → Show how long the system has been running
* `lscpu` → Display CPU information
* `man` → Access advanced command help

```

---
