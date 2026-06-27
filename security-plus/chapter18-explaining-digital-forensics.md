# Security+ Chapter 18 – Explaining Digital Forensics

## Main Idea

This chapter introduces digital forensics, the process of collecting, preserving, analyzing, and presenting digital evidence after a cybersecurity incident. Proper forensic procedures ensure evidence remains reliable for investigations and legal proceedings.

---

## Digital Forensics

Digital forensics is the process of identifying, collecting, preserving, analyzing, and reporting digital evidence.

### Objectives

- Determine what happened
- Identify the attacker
- Preserve digital evidence
- Support legal investigations
- Improve future security

---

## Forensic Process

Digital investigations follow a structured process to maintain evidence integrity.

### 1. Identification

Identify affected systems and potential sources of evidence.

### 2. Preservation

Protect evidence from modification or destruction.

### 3. Collection

Acquire digital evidence using approved forensic techniques.

### 4. Analysis

Examine collected data to determine attack activities.

### 5. Reporting

Document findings and present investigation results.

---

## Order of Volatility

Evidence should be collected from the most volatile data to the least volatile.

### Typical Order

- CPU registers and cache
- RAM (Memory)
- Running processes
- Network connections
- Temporary files
- Hard drives
- Archived backups

---

## Types of Digital Evidence

### Volatile Evidence

Exists only while a system is powered on.

**Examples:**

- RAM contents
- Active network connections
- Running processes

### Non-Volatile Evidence

Remains after the system is powered off.

**Examples:**

- Hard drives
- SSDs
- USB storage
- Log files

---

## Chain of Custody

Chain of Custody documents every person who handles digital evidence.

### Purpose

- Preserve evidence integrity
- Prevent tampering
- Support legal admissibility

### Documentation Includes

- Date and time
- Collector name
- Evidence description
- Transfer records

---

## Forensic Acquisition

Evidence should be collected without modifying the original data.

### Disk Imaging

Creates an exact bit-by-bit copy of storage media.

### Memory Capture

Captures volatile memory before shutdown.

### Log Collection

Collects operating system, application, and security logs.

---

## Hashing

Hashing verifies that evidence has not changed during the investigation.

### Common Algorithms

- SHA-256
- SHA-512
- MD5 (legacy verification)

### Benefits

- Verify integrity
- Detect modifications
- Validate forensic images

---

## Write Blockers

Write blockers prevent accidental modification of storage devices during forensic analysis.

### Benefits

- Protect original evidence
- Preserve integrity
- Support legal investigations

---

## File Recovery

Deleted files can often be recovered if storage sectors have not been overwritten.

### Common Sources

- Hard drives
- SSDs
- USB flash drives
- Memory cards

---

## Log Analysis

System logs provide valuable evidence during investigations.

### Common Log Sources

- Operating system logs
- Firewall logs
- Authentication logs
- Web server logs
- SIEM events

---

## Network Forensics

Network forensics investigates network communications.

### Evidence Sources

- Packet captures
- Firewall logs
- IDS/IPS alerts
- Router logs

### Objectives

- Identify attackers
- Trace attack paths
- Analyze malicious traffic

---

## Malware Analysis

Malware analysis determines how malicious software operates.

### Static Analysis

Examines malware without executing it.

### Dynamic Analysis

Executes malware inside an isolated sandbox.

### Goals

- Identify behavior
- Discover indicators of compromise (IOCs)
- Understand attack techniques

---

## Forensic Reporting

Every investigation should conclude with a detailed report.

### Report Contents

- Executive summary
- Timeline of events
- Evidence collected
- Analysis results
- Conclusions
- Recommendations

---

## Legal Considerations

Digital evidence must remain admissible in court.

### Requirements

- Proper Chain of Custody
- Evidence integrity
- Authorized collection
- Complete documentation

---

## Digital Forensics Best Practices

- Preserve original evidence
- Create forensic images
- Verify evidence using hashes
- Maintain Chain of Custody
- Document every investigation step
- Analyze evidence in isolated environments

---

## Key Takeaway

Digital forensics provides a structured methodology for investigating cybersecurity incidents. Proper evidence preservation, forensic imaging, hashing, log analysis, and Chain of Custody ensure investigations remain accurate, reliable, and legally defensible.
