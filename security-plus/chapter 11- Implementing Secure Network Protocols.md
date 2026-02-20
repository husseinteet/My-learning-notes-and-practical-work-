# Chapter11  Implementing Secure Network Protocols.

---

## Network Address Allocation

Network address allocation is the process of assigning unique IP addresses to devices on a network to enable communication.

### Types of IP Allocation

- **Static IP Address**
  - Manually configured
  - Does not change
  - Used for servers, printers, infrastructure devices

- **Dynamic Host Configuration Protocol (DHCP)**
  - Automatically assigns IP addresses
  - Reduces administrative overhead
  - Uses lease-based assignment

---

## Rogue DHCP Servers

A rogue DHCP server is an unauthorized DHCP server that assigns incorrect IP configurations.

### Risks:
- Man-in-the-Middle (MITM) attacks
- Network disruption
- Traffic redirection
- Data interception

---

## Domain Name Resolution (DNS)

DNS translates human-readable domain names (example.com) into IP addresses.

---

## Domain Hijacking

Domain hijacking occurs when an attacker gains unauthorized control of a domain.

### Causes:
- Weak passwords
- Phishing attacks
- Social engineering
- Registrar vulnerabilities

---

## DNS Poisoning (DNS Spoofing)

An attack that corrupts DNS cache to redirect users to malicious websites.

### How it Works:
- Cache poisoning
- Exploiting DNS vulnerabilities
- Man-in-the-Middle attacks

---

## DNS Security

DNS security protects the integrity, confidentiality, and availability (CIA) of DNS services.

### Protects Against:
- DNS spoofing
- Cache poisoning
- DDoS attacks

---

## Secure Directory Services

Directory services manage identities and access control.

### LDAP (Lightweight Directory Access Protocol)
- Accesses and manages directory services
- Uses Distinguished Names (DN)
- Stores attribute-value pairs

---

## Time Synchronization

Time synchronization ensures systems share the same time reference.

### Critical Services:
- Authentication
- Logging
- Backups
- Task scheduling

### Network Time Protocol (NTP)
- Stratum 1 servers (primary time source)
- Stratum 2 servers (secondary)
- Simple NTP (clients)

---

## SNMP Security

Simple Network Management Protocol (SNMP) monitors network devices.

- **SNMP v1/v2**
  - Weak authentication
  - No encryption

- **SNMP v3**
  - Authentication
  - Encryption
  - Secure configuration

---

## Transport Layer Security (TLS)

TLS is a cryptographic protocol that secures communication over networks.

### Provides:
- Confidentiality
- Integrity
- Authentication

SSL is the predecessor of TLS (deprecated).

---

## File Transfer Services

### FTP (File Transfer Protocol)
- Port 21 (control)
- Port 20 (data)
- Not encrypted

### SFTP (SSH File Transfer Protocol)
- Port 22
- Encrypted via SSH
- Secure file management

---

## Email Services

### SMTP
- Sends email between servers
- Port 25

### POP3
- Port 110 (standard)
- Port 995 (secure)

### IMAP
- Port 143 (standard)
- Port 993 (secure)

### S/MIME
- End-to-end encryption
- Digital signatures
- Uses PKI certificates

---

## Voice and Video Security

### VoIP / VTC Security Components:
- Session control
- Data transport
- Quality of Service (QoS)

### SIP (Session Initiation Protocol)
- Port 5060 (standard)
- Port 5061 (secure)

---

## TLS VPN

TLS VPN uses TLS protocol to create secure tunnels.

### Features:
- PKI authentication
- Encrypted tunnel
- Supports TCP or UDP

### SSTP
- Encapsulates PPP over HTTPS
- Secure remote access

---

## IPsec (Internet Protocol Security)

Secures IP communications.

### Authentication Header (AH)
- Provides integrity
- No encryption

### Encapsulation Security Payload (ESP)
- Encryption
- Authentication
- Integrity

### Modes:
- Transport Mode (host-to-host)
- Tunnel Mode (gateway-to-gateway)

---

## Internet Key Exchange (IKE)

Used to establish secure IPsec connections.

### Phase 1
- Authentication (PKI or pre-shared key)

### Phase 2
- Negotiates cipher suites
- Defines AH or ESP usage

---

## VPN Client Configuration

Requires:
- VPN gateway address
- Security type
- Credentials
- Client certificate (if required)

---

## Remote Desktop

Remote access to systems.

### RDP (Remote Desktop Protocol)
- Connect to physical machines
- RDP Gateway for secure remote access

---

## Out-of-Band (OOB) Management

Used for managing systems outside the production network.

### Includes:
- Serial console
- Modem access
- Virtual terminal

---

## Jump Servers

A hardened server used as an intermediary.

- Accepts SSH/RDP from secure admin workstations (SAWs)
- Forwards connections internally
- Internal servers only accept connections from jump server

---

## Secure Shell (SSH)

Secure remote administration protocol.

### Authentication Methods:
- Username/password
- Public key authentication
- Kerberos

### Key Management:
- Host key identifies server
- Public/private key pairs
- Keys must be securely stored and rotated
