# Systems as Attack Vectors

**Platform:** TryHackMe | **Path:** SOC Level 1

---

## The Core Idea

Training employees to spot phishing is important — but it means nothing if the systems themselves are vulnerable. Attackers do not always need a human to open the door. If the lock is weak enough, they walk right through.

Unlike human-targeted attacks, system attacks happen silently, without the victim doing anything wrong. A single breached server can compromise thousands of accounts at once — far more damaging than tricking one person into giving up their password.

---

## Why Systems Are Targeted

The value of a breached system depends entirely on what it holds or what it connects to.

| Breached System | What the Attacker Gains |
|---|---|
| Student's personal laptop | Stolen gaming accounts, PC added to a botnet |
| Bank IT administrator's laptop | Direct path into internal banking infrastructure |
| Law firm's mail server | Access to all mailboxes — used for blackmail |
| Industrial network server | Ransomware deployed across the entire network |
| Government website panel | Website defacement or politically motivated damage |

---

## How Systems Are Attacked

### Human-Led Attacks
Users are often the starting point — not because they are negligent, but because attackers exploit common habits:
- Plugging in a malicious USB found in a parking lot
- Downloading software from pirated sources
- Reusing weak passwords across multiple accounts

> **81% of breaches involve stolen or weak passwords.** Check if your passwords have been exposed at [haveibeenpwned.com](https://haveibeenpwned.com/Passwords)

### Software Vulnerabilities
Every piece of software contains flaws. Some are discovered quickly, others take decades.

- In 2024, over **40,000 CVEs** were published
- More than **300** were actively exploited in real attacks
- **Shellshock** — a critical Linux vulnerability — existed from **1992** but was not discovered until **2014**

When attackers find a vulnerability before anyone else, it is called a **zero-day**. There is no patch yet, and only strong detection capabilities can catch the exploitation in time.

Once a vulnerability is made public, it receives a **CVE number** and a race begins — attackers develop exploits while defenders rush to patch.

### Supply Chain Attacks
Every application on a device depends on hundreds of libraries and third-party components. If an attacker compromises one of those components and pushes a malicious update, every user of that software becomes a victim — without doing anything wrong.

Famous examples:
- **SolarWinds** — compromised software update affected thousands of organizations including US government agencies
- **3CX** — business communication software used as a delivery vehicle for malware

> Supply chain attacks are difficult to defend against because you cannot always control every library or dependency running on your systems.

---

## Software Vulnerabilities: Responding as a SOC Analyst

When a CVE is published, the official response is always a **patch** from the software vendor. While waiting for a patch — especially during zero-day scenarios — temporary measures help reduce exposure:

- Restrict access to the vulnerable system to trusted IPs only
- Apply any temporary workarounds provided by the vendor
- Block known attack patterns using an **IPS** or **WAF**

---

## Misconfigurations

A misconfiguration is not a bug in the code — it is a mistake in how the system was set up. These often happen because someone prioritized convenience over security.

**Real-world examples:**
- "123456" password exposed chat logs for **64 million** McDonald's job applicants
- A misconfigured AWS firewall led to a breach of **106 million** Capital One bank customers
- Improperly configured smart fridges silently recruited into large-scale botnets

### Responding to Misconfigurations

Unlike vulnerabilities, misconfigurations do not need a patch — they need a better setup. Proactive approaches include:

| Method | What It Does |
|---|---|
| **Penetration Testing** | Authorized ethical hackers simulate real attacks to find weaknesses before attackers do |
| **Vulnerability Scans** | Automated tools check for default passwords, outdated software, and known issues |
| **Configuration Audits** | Manual review of systems against established standards like CIS Benchmarks |

---

## Mitigation for Systems

| Measure | How It Helps |
|---|---|
| **Patch Management** | Tracks and applies updates to vulnerable systems promptly |
| **IT Training** | Reduces misconfiguration risk by educating the IT team on secure setup practices |
| **Network Protection** | Limits system access to trusted users and IP addresses |
| **Antivirus / EDR** | Detects and blocks many attack types before they execute |

---

## Key Takeaway

Attackers do not separate "hacking humans" from "hacking systems" — they use whichever path is easiest. As a SOC analyst, both attack surfaces are your responsibility: detect what mitigation misses, whether the entry point was a person or a vulnerable server.

---

## Key Terms

| Term | Definition |
|---|---|
| **CVE** | Common Vulnerabilities and Exposures — a public identifier for known security flaws |
| **Zero-Day** | A vulnerability unknown to the vendor, with no patch available yet |
| **Supply Chain Attack** | Compromising a trusted software component to reach all of its users |
| **Misconfiguration** | A security weakness caused by incorrect system setup, not a software bug |
| **Patch** | A software update that fixes a known vulnerability |
| **Botnet** | A network of compromised devices controlled remotely by an attacker |
| **Defacement** | Unauthorized modification of a website's content |
| **IPS** | Intrusion Prevention System — monitors and blocks malicious network traffic |
| **WAF** | Web Application Firewall — filters and blocks malicious web requests |
| **CIS Benchmarks** | Industry-standard guidelines for secure system configuration |
| **Penetration Testing** | Authorized simulated attack to identify security weaknesses |

