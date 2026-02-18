# 📘 Chapter 09 - Secure Network Design

## 🎯 Overview
This chapter covers secure network architecture, segmentation, routing security, wireless security, and network attack mitigation techniques.

---

# 🔐 Secure Network Design Principles

## Common Network Design Weaknesses
- Single points of failure
- Complex dependencies
- Prioritizing availability over confidentiality and integrity
- Overdependence on perimeter security

## Best Practice Architecture Guides
- Cisco SAFE Architecture
- Defined security zones within the network

---

# 🌐 Routing and Switching Fundamentals

## Forwarding
- Layer 2 forwarding (Switching)
- Layer 3 forwarding (Routing)

## Address Resolution Protocol (ARP)
- Maps IP addresses to MAC addresses

## Internet Protocol (IP)
- IPv4 and IPv6
- Network prefix and subnet mask

---

# 🧩 Network Segmentation

## Network Segment
- Devices communicate at Layer 2
- Broadcast domain

## Implementing Segmentation
- Separate unmanaged switches
- VLAN configuration on managed switches
- Mapping subnets to VLANs (Layer 3 segmentation)

---

# 🏢 Network Topology & Security Zones

## Topologies
- Physical topology
- Logical topology

## Security Zones
- Isolated segments with similar security requirements
- Inter-zone traffic filtered by firewall

### Main Zone Types
- Intranet (Private)
- Extranet
- Internet (Public)

---

# 🛡 Demilitarized Zone (DMZ)

- Isolates internet-facing hosts
- Internal communication should be restricted

## Bastion Hosts
- Minimal services
- Not fully trusted
- No internal credentials stored
- Separate DMZs for different functions

---

# 🔎 Screened Host Architecture

- Uses firewall + router filtering
- Adds additional protection layer
- Screens traffic before reaching internal systems

---

# 🌍 IPv6 Security Implications

- Often enabled by default
- Risk of unmanaged configurations
- IPv6-specific attack vectors

---

# 🏗 Modern Network Design Considerations

## Data Center & Cloud Design
- East-West Traffic (server-to-server)
- North-South Traffic (external to internal)
- East-West inspection challenges

## Zero Trust Model
- Do not rely solely on perimeter security
- Continuous/context-based authentication
- Microsegmentation

## Single Host Zones
- Isolate critical systems individually

---

# ⚠ Network Attacks

## Man-in-the-Middle (MITM)
- On-path interception
- Snooping
- Spoofing

## MAC Address Spoofing
- MAC addresses easily modified
- Used for impersonation

## ARP Poisoning
- Spoofed ARP replies
- Attacker masquerades as default gateway

## MAC Flooding
- Overwhelms switch memory
- Causes unicast flooding
- Enables sniffing

---

# 🔄 Loop Prevention

## Spanning Tree Protocol (STP)
- Prevents switching loops

## Broadcast Storms
- Amplified traffic due to loops

## BPDU Guard
- Disables port if STP traffic detected
- Protects PortFast access ports

---

# 🔐 Physical Port Security

## Port Hardening
- Secure switch hardware
- Disconnect unused ports
- Disable unused ports

## MAC Filtering & Limiting
- Configure permitted MAC addresses
- Limit number of MAC changes

## DHCP Snooping
- Prevent rogue DHCP servers
- Enables Dynamic ARP Inspection

---

# 🛣 Route Security

- Protect routing table integrity
- Prevent route injection
- Disable source routing
- Router patching and hardening

---

# 📶 Wireless Network Security

## WAP Placement Considerations
- SSID & BSSID
- Frequency bands & channels
- Co-channel interference (CCI)
- Adjacent channel interference (ACI)

## Site Surveys & Heat Maps
- Architecture plans
- Wi-Fi analyzers
- Channel overlap detection

---

# 📡 Wireless Controller & AP Security

- Multi-WAP WLAN configuration
- Hardware vs Software controllers
- Fat vs Thin APs
- Secure management interfaces

---

# 🔐 Wi-Fi Security Standards

## WPA2
- Uses AES (replaces RC4)

## WPA3
- SAE (Simultaneous Authentication of Equals)
- Enhanced Open
- Stronger cryptography
- Protected management frames

---

# 🔑 Wi-Fi Authentication Methods

## WPA2-PSK
- Passphrase generates PMK
- 4-way handshake
- Session key derivation

## WPA3-Personal
- SAE replaces 4-way handshake
- Dragonfly handshake
- PAKE authentication

---

# 📲 Wi-Fi Protected Setup (WPS)

- Simplifies Wi-Fi connection
- Methods:
  - Push Button Configuration (PBC)
  - PIN Method
- Security risk if PIN brute-forced

---

# 🏢 Enterprise Authentication (IEEE 802.1X)

- Uses EAP
- Integrated with RADIUS or TACACS+
- Generates session encryption keys

---

# 🔐 Extensible Authentication Protocol (EAP)

## EAP-TLS
- Mutual authentication
- Requires certificates on client & server

## PEAP
- TLS tunnel protects password
- Server certificate only

## EAP-TTLS
- Flexible inner authentication methods

---

# 🚨 Rogue Access Points & Evil Twins

## Rogue AP
- Unauthorized AP inside network

## Evil Twin
- Fake AP mimicking legitimate SSID
- Captures credentials

---

# 📡 Jamming Attacks

- Wireless DoS attack
- Interferes with frequency band
- Prevents communication

---

# 🌊 Distributed Denial of Service (DDoS)

- Overwhelms server/network with traffic

## DRDoS (Reflection/Amplification)
- Spoof victim IP
- Servers reflect traffic to victim

## Application Attacks
- Bogus DNS/NTP queries
- SYN flood attacks

---

# 🛡 DDoS Mitigation

- ACL filtering
- Remotely Triggered Black Hole (RTBH)
- Sinkhole routing
- Cloud-based mitigation services

---

# ⚖ Load Balancing

## Types
- Layer 4 load balancer
- Layer 7 load balancer

## Scheduling Methods
- Round Robin
- Best response time
- Weighted
- Health checks
- Source IP affinity

---

# 🔄 Clustering & High Availability

- Failover configuration
- Virtual IP
- CARP
- Active/Passive models
- Stateful application clustering

---

# 📊 Quality of Service (QoS)

- Prioritize critical traffic
- Manage:
  - Bandwidth
  - Latency
  - Jitter

## Traffic Marking
- DiffServ
- 802.1p

## Traffic Policing
- Enforce bandwidth limits

## Trust Boundaries
- Prevent abuse of QoS marking
- Protect management/security traffic
