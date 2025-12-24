# Security+ Chapter 03 – Performing Security Assessments

## Main Idea
This chapter explains how organizations assess their security posture by
identifying vulnerabilities, analyzing risks, and validating security controls
before attackers exploit weaknesses.

---

## Security Assessments
Security assessments are systematic evaluations used to identify weaknesses
in systems, networks, and applications.

Common assessment types include:
- Vulnerability assessments
- Penetration testing
- Security audits

---

## Network Reconnaissance
Network reconnaissance is the process of gathering information about a network
to identify potential vulnerabilities and attack surfaces.

---

## Common Reconnaissance Tools

- **Nmap:** Identifies live hosts, open ports, and running services.
- **Wireshark:** Captures and analyzes network traffic.
- **Netcat:** Tests network connections and data transfer.
- **Angry IP Scanner:** Quickly identifies active hosts on a network.
- **OpenVAS / Nessus:** Scans systems for known vulnerabilities.

---

## Network Diagnostic Commands

- **route:** Displays the local routing table.
- **traceroute / tracert:** Traces the path to a remote host.
- **pathping:** Measures latency and packet loss.
- **netstat:** Displays network connections and open ports.
- **nslookup:** Queries DNS servers.
- **dnsenum:** Collects DNS-related information.

---

## Packet and Protocol Analysis

- **Packet analysis:** Examines packet headers and payloads.
- **Protocol analysis:** Focuses on how network protocols operate.
- **Sniffers:** Tools used to capture network frames.
- **tcpdump:** Command-line packet capture and analysis tool.

---

## Packet Injection
Packet injection involves crafting and sending custom network packets,
often used during penetration testing.
**Examples:** Scapy, Hping.

---

## Exploitation Frameworks
Tools that assist security professionals in identifying and validating
vulnerabilities.

- **Metasploit Framework:** Develops and executes exploit code.
- **Sn1per:** Automated reconnaissance and vulnerability scanning tool.

---

## General Vulnerability Types

- Software code flaws (e.g., buffer overflows)
- Application vulnerabilities
- Operating system vulnerabilities
- Firmware vulnerabilities
- Weak host configurations (default passwords, open ports)
- Weak network configurations (insecure protocols, open Wi-Fi)
- Third-party risks (vendors, unsupported software)

---

## Vulnerability Scan Types

- **Network scans:** Open ports and misconfigurations
- **Host-based scans:** Missing patches and system flaws
- **Web application scans:** SQL injection, XSS (OWASP ZAP, Burp Suite)
- **Database scans:** Misconfigurations and weak permissions
- **Wireless scans:** Weak encryption and access points
- **Cloud scans:** Misconfigurations and access control issues

---

## CVE (Common Vulnerabilities and Exposures)
CVE provides publicly known vulnerability identifiers.
Each CVE ID uniquely identifies a specific security vulnerability.

---

## Scanning Approaches

- **Intrusive (Active) scanning:** Direct interaction with systems
- **Non-intrusive (Passive) scanning:** Collects data without direct interaction

---

## Scan Accuracy

- **False positive:** Vulnerability reported but not present
- **False negative:** Vulnerability present but not detected

---

## Penetration Testing
Penetration testing simulates real-world attacks to identify and validate
security weaknesses.

### Types of Penetration Testing
- **Black box:** No prior system knowledge
- **White box:** Full system knowledge
- **Gray box:** Partial system knowledge

---

## Phases of Penetration Testing

1. Planning and preparation
2. Scanning and enumeration
3. Exploitation
4. Post-exploitation
5. Reporting and recommendations

---

## Penetration Testing Attack Lifecycle

- Initial exploitation
- Command and control establishment
- Lateral movement
- Privilege escalation
- Cleanup

---

## Key Takeaway
Security assessments help organizations proactively identify vulnerabilities,
reduce risk, and improve overall security posture.
