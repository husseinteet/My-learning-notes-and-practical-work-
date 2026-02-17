# 📘 Chapter 08 - Implementing Identity and Account Management Controls

## 🎯 Overview
This chapter covers identity and account management controls used to secure systems, manage privileges, enforce authentication policies, and implement access control models.

---

# 🔐 Privileged Access Management (PAM)

## Benefits
- Mitigate insider threats
- Enforce separation of duties
- Implement least privilege
- Assign sufficient permissions only
- Reduce risk from compromised accounts

---

# 👤 Security Account Types & Credential Management

## Standard Users
- Limited privileges
- Cannot change system configuration
- Restricted to account profile

## Guest Account
- Anonymous logon (no credentials)
- Unauthenticated access
- Should have very limited privileges or be disabled

## Credential Management Policies
- Password policies protect access
- Prevent unauthorized compromise

---

# 👥 Security Groups & Privileges

## User-Assigned Privileges
- Permissions assigned directly to users
- Difficult to manage in large environments

## Group-Based Privileges
- Permissions assigned to security groups
- Users inherit group permissions

### Issues
- Users may inherit multiple permissions

---

# 👑 Administrator / Root Accounts

- High-privilege accounts
- Unrestricted access to system resources
- Prime target for attackers
- Often disabled or restricted after installation

---

# ⚙ Service Accounts

- Used by applications and services
- No user interaction required

## Windows Service Accounts
- System
- Local Service
- Network Service

## Linux Service Accounts
- Used to run services
- Shell access typically denied

---

# 👥 Shared & Generic Accounts

## Shared Accounts
- Credentials known by multiple users

## Generic Accounts
- Default OS accounts
- May use default passwords
- High security risk

---

# 🔑 SSH Keys & Third-Party Credentials

## Secure Shell (SSH)
- Host key identifies server
- User key pair authenticates to server
- Server stores public keys
- Keys must be managed securely

## Third-Party Credentials
- Cloud passwords and API keys
- Vulnerable to accidental disclosure

---

# 🏷 Account Attributes & Access Policies

## Account Attributes
- Security ID (SID)
- Account name
- Credentials
- Extended profile attributes
- Per-application settings

## Access Policies
- File permissions
- Access rights
- Group Policy Objects (GPOs)

---

# 🔐 Password Policy Settings

- Minimum length
- Complexity requirements
- Password aging
- Password history and reuse prevention
- NIST guidance
- Password hints

---

# 🚫 Account Restrictions

## Network Restrictions
- VLAN / IP subnet restrictions
- Remote IP restrictions
- Interactive vs remote logon control

## Geolocation Restrictions
- IP-based location checks
- Location services validation

## Time-Based Restrictions
- Logon hours
- Logon duration limits
- Impossible travel detection

---

# 📊 Account Auditing & Recertification

## Auditing
- Monitor file access
- Track failed login attempts
- Monitor resource access

## Recertification
- Monitor privilege usage
- Grant or revoke privileges
- Coordinate between IT and HR

---

# 🔎 Account Permissions

## Risks
- Insufficient permissions
- Excessive permissions
- Privilege escalation

## Tools
- Permission auditing tools

---

# 📋 Usage Auditing

- Account logon events
- Account management events
- Process creation
- Object access (file systems and shares)
- Changes to audit policy
- System security and integrity changes

---

# 🔒 Account Lockout & Disablement

## Disablement
- Manual re-enable required
- Often combined with remote logoff

## Lockout
- Temporary login restriction
- Automatically re-enabled after defined period

---

# 🛂 Access Control Models

## Discretionary Access Control (DAC)
- Based on ownership
- Uses ACLs
- Vulnerable if privileged account is compromised

## Role-Based Access Control (RBAC)
- Centralized control
- Users assigned to roles
- Users inherit role permissions

## Mandatory Access Control (MAC)
- Uses labels and clearance levels
- Strict system-enforced policies

## Attribute-Based Access Control (ABAC)
- Based on subject, object, and contextual attributes
- Supports conditional access

## Rule-Based Access Control
- System-defined rules
- Continuous authentication
- Includes User Account Control (UAC)

---

# 🗂 File System Security

## Access Control List (ACL)
- Defines permissions for users and groups

## Access Control Entry (ACE)
- Individual permission entry inside ACL

## Linux Permissions
- Symbolic: rwx
- User / Group / Others
- Octal: r=4, w=2, x=1

---

# 🗄 Directory Services

- Database of subjects (users, computers, groups, services)
- Authorization through ACLs
- X.500 and LDAP
  - Distinguished Names (DN)
  - Attribute-value pairs

---

# 📜 Conduct Policies

## Acceptable Use Policy (AUP)
- Defines employee use of company hardware and software

## Rules of Behavior
- Professional conduct requirements
- Social media guidelines
- Additional clauses for privileged users

## Bring Your Own Device (BYOD)
- Policies for personally owned devices
