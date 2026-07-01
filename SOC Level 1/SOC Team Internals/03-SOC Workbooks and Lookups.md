# Alert Triage — Lookups and Workbooks

**Platform:** TryHackMe | **Path:** SOC Level 1

---

## The Core Problem This Room Solves

When an alert fires, the raw data alone rarely tells the full story. An alert showing "user G.Baker logged into HQ-FINFS-02 and shared a file with R.Lund" raises more questions than it answers:

- Who is G.Baker? What is their role and normal working hours?
- What is HQ-FINFS-02? What does it store and who is authorized to access it?
- Is R.Lund someone who would legitimately receive this data?

Without answers to these questions, you cannot make a reliable verdict. This room covers the three tools that give you that context: **Identity Inventory**, **Asset Inventory**, and **Network Diagrams** — and how **SOC Workbooks** turn those tools into a repeatable investigation process.

---

## Identity Inventory

An identity inventory is a catalogue of every user and service account in the organization, along with their details: role, department, access privileges, working hours, and contact information.

During an investigation, it answers the "who" question — is this person expected to be doing this? Do they have a business reason to access this system?

**Common Sources:**

| Source | Examples | Notes |
|---|---|---|
| **Active Directory** | On-prem AD, Entra ID | The most common source — AD is itself an identity database |
| **SSO Providers** | Okta, Google Workspace | Cloud alternative to AD, easy to search |
| **HR Systems** | BambooHR, SAP, HiBob | Employee-only data, but often the most complete |
| **Custom Solutions** | CSV or Excel sheets | Still common in smaller organizations |

---

## Asset Inventory

Asset inventory (also called asset lookup) is a list of all computing resources in the environment — servers, workstations, and the details that matter: what they run, where they are, who manages them, and what data they hold.

During an investigation, it answers the "what" question — what is this machine, and does it make sense for this user to be interacting with it?

**Common Sources:**

| Source | Examples | Notes |
|---|---|---|
| **Active Directory** | On-prem AD, Entra ID | Also doubles as a solid asset database |
| **SIEM / EDR** | Elastic, CrowdStrike | Agents collect host details automatically |
| **MDM Solutions** | MS Intune, Jamf | Purpose-built for listing and managing endpoints |
| **Custom Solutions** | CSV or Excel sheets | Common fallback when dedicated tooling isn't available |

---

## Network Diagrams

When alerts come from firewall logs or involve IP addresses and subnets, you need a visual map of the network to make sense of the traffic. A network diagram shows the physical and logical layout of the organization: locations, subnets, services running on specific ports, and how different segments connect.

**Example Investigation Using a Network Diagram:**

A chain of alerts reveals:
1. `103.61.240.174` repeatedly connects to the corporate firewall on port `TCP/10443`
2. After a successful connection, it gets assigned internal IP `10.10.0.53`
3. That IP begins scanning the `172.16.15.0/24` subnet — no open ports found
4. The same IP shifts to scanning `172.16.23.0/24`

Without a network diagram, these are just numbers. With one, the attack path becomes clear:
- Port 10443 is the VPN service → attacker brute-forced VPN credentials
- After gaining VPN access, they were assigned an IP from the VPN subnet
- They then attempted lateral movement, first toward the Database subnet (blocked by firewall), then pivoting to the Office subnet

Network diagrams turn raw IP data into a reconstructed attack story.

---

## SOC Workbooks

A SOC workbook (also called a playbook, runbook, or workflow) is a structured step-by-step guide for investigating and resolving a specific type of alert. Senior analysts write them to support L1 analysts — ensuring nothing critical gets skipped during triage, regardless of experience level.

Following a workbook is not optional for L1 analysts. In many teams, it is required precisely because skipping steps is how real threats get missed.

### Workbook Structure

Most workbooks follow three logical phases:

**1. Enrichment**
Before investigating anything, gather context. Use threat intelligence platforms and identity/asset inventory to understand who and what is involved. Going straight into logs without this context wastes time.

**2. Investigation**
With context in hand, dig into SIEM or EDR logs. Look at what happened, what happened around it, and whether it aligns with expected behavior for this user, system, or network segment. Make a verdict: True Positive or False Positive.

**3. Escalation**
If the alert is confirmed as a real threat, escalate to L2 with a clear summary of findings. If there's ambiguity — like a login from an unusual location that might just be travel — communicate directly with the affected user or their manager before closing.

### The Process of Gathering Context

The act of pulling together user, host, and IP context from threat intelligence and inventory sources is called **Enrichment**. This step happens before investigation, not during it — having the full picture upfront makes the investigation itself much faster and more accurate.

---

## Different Approaches to Workbooks

Not every team builds workbooks the same way:

| Approach | Description | Best For |
|---|---|---|
| **Comprehensive** | Hundreds of detailed workbooks, one per detection rule — close to SOAR automation logic | Large, mature SOC teams |
| **High-Level** | A few broad workbooks for the most common attack vectors, relying more on analyst judgment | Smaller teams or those still building their processes |

As an L1 analyst, the skill to develop is the ability to break any investigation into modular steps — even when a formal workbook doesn't exist yet.

---

## Key Terms

| Term | Definition |
|---|---|
| **Identity Inventory** | A catalogue of user and service accounts and their attributes (role, access, department) |
| **Asset Inventory** | A list of all computing resources with details about their purpose and location |
| **Network Diagram** | A visual map of the organization's network — subnets, services, and how they connect |
| **SOC Workbook** | A structured investigation guide for a specific alert type (also: playbook, runbook, workflow) |
| **Enrichment** | The process of gathering user, host, or IP context using threat intelligence and lookups |
| **Active Directory (AD)** | Microsoft's identity and access management service — also a source for both identity and asset inventory |
| **SSO** | Single Sign-On — cloud-based identity management (e.g. Okta, Google Workspace) |
| **MDM** | Mobile Device Management — used to track and manage endpoints |
| **SOAR** | Security Orchestration, Automation and Response — can automate workbook-style investigation steps |

