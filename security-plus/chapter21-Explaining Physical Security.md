# Chapter 21 - Explaining Physical Security

**Course:** CompTIA Security+ | **Source:** Ahmad Hassan Al-Mashaikh

---

## Overview

Digital defenses mean nothing if someone can walk into a server room and unplug a machine. Physical security is the foundation everything else sits on — it controls who can access spaces, devices, and data in the real world.

This chapter covers two areas: securing the physical site itself, and securing the hardware and data hosted within it.

---

## Section 1: Physical Site Security Controls

### The AAA Framework Applied Physically

Physical access control follows the same principles as logical access control:

| Control | What It Means Physically |
|---|---|
| **Authentication** | Access lists and ID mechanisms that verify who is allowed through a barrier |
| **Authorization** | Barriers and defined entry/exit points that restrict where an authenticated person can go |
| **Accounting** | Logs of when entry/exit points were used — used to detect and investigate breaches |

Technical tools supporting this: Firewalls, EDR, Data Encryption, ACLs, Network Segmentation, Patch Management.

---

### Site Layout, Fencing, and Lighting

**Site Layout**
The physical design of a facility should be intentional, not accidental:
- Zone-based design that controls traffic flow and supports surveillance coverage
- Proper signage to guide authorized personnel and deter unauthorized access
- Industrial camouflage for sensitive facilities to reduce their visibility as targets

**Barricades and Entry Points**
- Bollards — concrete or steel posts that prevent vehicle-based attacks on entry points
- Controlled entry/exit points to funnel access through monitored locations

**Fencing**
Physical perimeter barrier — the first line of defense before someone reaches the building.

**Lighting**
- Makes staff feel safer and more alert
- Directly supports surveillance camera effectiveness — cameras are useless in the dark

---

### Gateways and Locks

Lock types range from basic to highly secure:

| Type | Examples |
|---|---|
| **Physical** | Conventional locks, deadbolts |
| **Electronic** | Cipher/combination pads, magnetic swipe cards |
| **Smart / Proximity** | RFID cards, proximity readers |
| **Biometric** | Fingerprint, retina, or facial recognition |
| **Mantrap / Vestibule** | Two-door entry — second door only opens after first closes and identity is confirmed |
| **Turnstile** | Controls one-person-at-a-time entry to prevent tailgating |
| **Cable Lock** | Physically secures hardware like laptops to desks |

---

### Physical Attacks Against Smart Cards and USB

**Smart Card Attacks**
- **Cloning** — duplicating a card's data onto a blank card
- **Skimming** — secretly reading card data using a hidden reader placed near a legitimate one
- Different card types carry different vulnerability levels

**Malicious USB / Juice Jacking**
- Attackers leave infected USB drives in public spaces (USB drop)
- Juice jacking uses public charging ports to deliver malware or steal data
- **Defense:** USB data blockers — allow charging while blocking data transfer

---

### Alarm and Sensor Systems

| Sensor Type | How It Works |
|---|---|
| **Circuit (open/closed)** | Detects if a barrier has been breached — door or window opened |
| **Motion Detection** | Radar or infrared — detects movement in a defined space |
| **Noise Detection** | Picks up sounds like breaking glass |
| **Proximity Reader** | Triggers alerts when an unauthorized device or person gets too close |
| **Duress Alarm** | Fixed or mobile — allows staff to silently signal an emergency |

---

### Security Guards and Cameras

**Remote Surveillance Tools:**
- CCTV / Video monitoring
- Motion recognition — alerts when movement is detected in restricted areas
- Object detection — identifies specific items or behaviors
- Robot sentries — automated physical patrol units
- Drones / UAVs — aerial surveillance for large or outdoor facilities

---

### Reception Personnel and ID Badges

- Reception staff act as the human layer of access control
- ID badges provide visual identification and can carry electronic access data
- Visitor logs and escort policies reduce insider threat and unauthorized access risks

---

## Section 2: Physical Host Security Controls

### Secure Areas

Hardware and sensitive systems require physically protected environments:

| Location Type | Purpose |
|---|---|
| Server rooms / Data centers | Controlled environments for critical infrastructure |
| Lockable cabinets | Secure individual servers or network equipment |
| Colocation cages | Isolated space within a shared data center |
| Air gaps | Complete physical isolation from external networks |
| Demilitarized zones (DMZ) | Controlled buffer zones between network segments |
| Safes and Vaults | Physical storage for backup media, encryption keys, or critical documents |

Environmental monitoring in secure areas tracks: temperature, humidity, airflow, water leakage, and power line voltages.

---

### Protected Distribution and Faraday Cages

**Protected Distribution System (PDS)**
Physically secured cable routing that:
- Prevents eavesdropping on network traffic traveling through cables
- Prevents or delays cable-cutting denial of service attacks

**Faraday Cage**
A shielded enclosure that blocks electromagnetic signals from entering or leaving.
- Prevents wireless signals, RF attacks, and electromagnetic eavesdropping
- Related standard: **TEMPEST** (Transient Electromagnetic Pulse Emanation Standard)

---

### Hot and Cold Aisles

Data centers use a hot/cold aisle design to manage heat from server hardware efficiently:

- **Cold aisle** — server fronts face this aisle, intake cool air
- **Hot aisle** — server backs face this aisle, exhaust hot air toward HVAC
- Servers are arranged back-to-back to keep hot exhaust away from cold intake
- Prevents cooled air from mixing with warmed exhaust air, improving cooling efficiency

---

### Fire Detection and Suppression

**Fire Safety Measures:**
- Fire exits and clearly communicated evacuation procedures
- Fire-resistant building construction materials
- Smoke and flame detectors with automatic alarm triggers

**Suppression:**
- **Class C fire extinguishers** — required for electrical equipment (standard water extinguishers conduct electricity)
- Gas-based suppression systems in server rooms — suppress fire without damaging equipment with water

---

### Secure Data Destruction

When storage media reaches end of life, simply deleting files is not enough — data remnants can be recovered.

**Destruction Methods:**

| Method | Description |
|---|---|
| **Burning / Incineration** | Complete physical destruction of the media |
| **Shredding / Pulping** | Mechanically destroys the physical storage medium |
| **Pulverizing** | Grinding media into fine particles |
| **Degaussing** | Using a strong magnetic field to erase magnetic storage (HDDs, tapes) |

Third-party destruction services can provide **certificates of destruction** as documented proof.

---

### Data Sanitization Tools

For media that needs to be reused rather than destroyed:

| Method | How It Works |
|---|---|
| **Zero Filling** | Overwrites all data with zeros — one pass |
| **Multiple Passes** | Overwrites data repeatedly with random patterns for stronger sanitization |
| **Secure Erase (SE)** | Built-in firmware command for HDDs and SSDs/flash media |
| **Instant Secure Erase (ISE) / Crypto Erase** | Used on self-encrypting drives (SED) — deletes the encryption key, making all data unreadable instantly |

---

## Key Terms

| Term | Definition |
|---|---|
| **Mantrap / Vestibule** | Two-door entry system that allows only one person through at a time |
| **Bollard** | Physical barrier (post) that prevents vehicle access |
| **Tailgating** | Unauthorized person following an authorized person through a secured entry |
| **Juice Jacking** | Attack using a compromised charging port to deliver malware or steal data |
| **Skimming** | Reading card data covertly using a hidden reader |
| **Faraday Cage** | Enclosure that blocks electromagnetic signal transmission |
| **TEMPEST** | Standard for controlling electromagnetic emissions from equipment |
| **PDS** | Protected Distribution System — secured physical cabling infrastructure |
| **Degaussing** | Erasing magnetic storage using a strong magnetic field |
| **SED** | Self-Encrypting Drive — hardware-level encryption with Instant Secure Erase support |
| **Hot/Cold Aisle** | Data center layout design to optimize airflow and cooling efficiency |
| **Air Gap** | Complete physical and network isolation of a system |

