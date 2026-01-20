

---


````md
# Chapter 3 – Scripting Basics & Bash Automation

## What is Scripting
- Scripting refers to writing small programs to **automate tasks**
- Commonly used to execute repetitive or administrative tasks efficiently

## Why Use Scripting
- **Automation**: Automates repetitive tasks, saving time and reducing human error
- **Efficiency**: Executes complex operations with a single command
- **Flexibility**: Easily adaptable to different tasks and environments
- **Integration**: Scripts can interact with other applications and systems

## Common Scripting Languages
- **Bash**: Used in Unix/Linux systems for automating command-line tasks
- **Python**: Used in web development, automation, and data analysis
- **JavaScript**: Used to create interactive web pages
- **PowerShell**: Used in Windows environments for system administration and automation

## Core Scripting Concepts
- **Variables**: Store data used in a script
- **Control Structures**: Conditions (`if`, `switch`) and loops (`for`, `while`)
- **Functions**: Reusable blocks of code that perform a specific task
- **Input & Output**: Capture user input and display results

---

## Simple Bash Script (Hello World)

### Steps
1. Create the script file
```bash
nano my-script.sh
````

2. Add the shebang at the top

```bash
#!/bin/bash
```

3. Write the command

```bash
echo "Hello World"
```

4. Give execute permission

```bash
chmod 777 my-script.sh
```

5. Run the script

```bash
./my-script.sh
```

---

## Bash Backup Script

```bash
#!/bin/bash

SRC_DIR="$1"
DEST_DIR="$2"

if [ -z "$SRC_DIR" ] || [ -z "$DEST_DIR" ]; then
    echo "Usage: $0 <source_directory> <destination_directory>"
    exit 1
fi

TIMESTAMP=$(date +"%Y%m%d_%H%M%S")
BACKUP_FILE="backup_$TIMESTAMP.tar.gz"

tar -czvf "$DEST_DIR/$BACKUP_FILE" "$SRC_DIR"

echo "Backup of $SRC_DIR created at $DEST_DIR/$BACKUP_FILE"
```

---

## Collect Device Information Script

```bash
#!/bin/bash

OUTPUT_FILE="device_info.txt"

{
    echo "Device Information"
    echo "Hostname: $(hostname)"
    echo "Operating System: $(uname -o)"
    echo "Kernel Version: $(uname -r)"

    echo "CPU Information:"
    lscpu | grep -E 'Model name|Socket|Core|Thread'

    echo "Memory Usage:"
    free -h

    echo "Network Interfaces:"
    ip a | grep -E '^[0-9]+:'
} > "$OUTPUT_FILE"

echo "Device information saved to $OUTPUT_FILE"
```

---

## Collect Installed Tools Script

```bash
#!/bin/bash

OUTPUT_FILE="installed_tools.txt"

{
    if command -v apt &> /dev/null; then
        dpkg --get-selections | grep -v deinstall
    elif command -v yum &> /dev/null; then
        yum list installed
    elif command -v dnf &> /dev/null; then
        dnf list installed
    elif command -v pacman &> /dev/null; then
        pacman -Q
    else
        echo "No supported package manager found"
    fi
} > "$OUTPUT_FILE"

echo "Installed tools saved to $OUTPUT_FILE"
```

---

## Collect User Profile File Information

```bash
#!/bin/bash

OUTPUT_FILE="user_profile_files_info.txt"
PROFILE_DIR="$HOME"

{
    echo "File Name | Size | Type | Last Modified"
    find "$PROFILE_DIR" -maxdepth 1 -type f | while read -r file; do
        echo "$(basename "$file") | $(du -h "$file" | cut -f1) | $(file -b "$file") | $(stat -c '%y' "$file")"
    done
} > "$OUTPUT_FILE"

echo "User profile file information saved to $OUTPUT_FILE"
```

---

## Nmap Network Scan Script

```bash
#!/bin/bash

OUTPUT_FILE="nmap_scan_results.txt"
NETWORK="192.168.1.0/24"

{
    nmap -sn "$NETWORK"
    nmap -p 1-65535 "$NETWORK"
} > "$OUTPUT_FILE"

echo "Nmap scan results saved to $OUTPUT_FILE"
```

---

## Script to Create Files

```bash
#!/bin/bash

echo "This is the first file." > file1.txt
echo "This is the second file." > file2.txt
echo "This is the third file." > file3.txt

echo "Files created successfully"
```

---

## Monitor User Activity Script

```bash
#!/bin/bash

LOG_FILE="$HOME/user_activity_log.txt"

{
    echo "User Activity Log"
    last | head -n -2
    history | tail -n 20
} > "$LOG_FILE"

echo "User activity logged to $LOG_FILE"
```

---

## TCP and UDP Monitoring Script

```bash
#!/bin/bash

OUTPUT_FILE="network_traffic_log.txt"

if ! command -v tcpdump &> /dev/null; then
    echo "tcpdump is not installed"
    exit 1
fi

sudo tcpdump -i any -n -c 1000 'tcp or udp' > "$OUTPUT_FILE"

echo "Network traffic saved to $OUTPUT_FILE"
```

---
