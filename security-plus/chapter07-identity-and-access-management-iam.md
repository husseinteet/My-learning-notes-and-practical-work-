# Chapter 7 – Identity and Access Management (IAM)

## Introduction to IAM
Identity and Access Management (IAM) is a framework of policies, processes, and technologies that ensures the right individuals or entities have appropriate access to organizational resources.

IAM helps control:
- Who can access resources
- What actions they can perform
- How access is monitored and audited

---

## Core IAM Concepts (AAA Model)

- **Subjects**: Users or software requesting access
- **Objects**: Resources such as servers, networks, or data
- **Identification**: Associating a subject with a valid account
- **Authentication**: Verifying the identity of the subject
- **Authorization**: Assigning rights, permissions, or privileges
- **Accounting**: Auditing and logging account activity

---

## Authentication Design
Authentication design focuses on creating secure methods to verify user identity before granting access to resources.

Strong authentication mechanisms reduce the risk of unauthorized access.

---

## Multi-Factor Authentication (MFA)
MFA requires two or more verification factors before granting access.

### Authentication Factors
- **Something you know** (PIN, password)
- **Something you have** (smart card, smartphone, hardware token)
- **Something you are** (biometrics)

### How MFA Works
1. User initiates login
2. First factor verification (username and password)
3. Second factor verification (e.g., SMS code or app-based OTP)
4. Access is granted or denied

---

## Authentication Attributes
Authentication may also include contextual attributes:

- **Somewhere you are**
  - Geolocation services
  - IP address location
  - Switch port or VLAN assignment

These are often used in adaptive or risk-based authentication.

---

## Kerberos Authentication
Kerberos is a secure network authentication protocol that uses secret-key cryptography to authenticate users over insecure networks.

### Key Components
- **Key Distribution Center (KDC)**
  - Authentication Server (AS)
  - Ticket Granting Service (TGS)

### Kerberos Process
1. User requests a Ticket Granting Ticket (TGT)
2. KDC verifies credentials and issues TGT + session key
3. User requests service ticket from TGS
4. TGS issues service ticket + session key
5. User presents ticket to access the service

Kerberos provides:
- Mutual authentication
- Ticket-based access
- Protection against replay attacks

---

## Password Cracking
Password crackers attempt to recover passwords from stored or transmitted data.

### Attack Types & Tools

#### Brute Force Attacks
- Hashcat
- John the Ripper

#### Dictionary Attacks
- Cain & Abel
- Aircrack-ng

#### Rainbow Table Attacks
- RainbowCrack

---

## Secure Password Storage Solutions

### Hardware Solutions
- **Hardware security tokens**
  - Generate one-time passwords (OTP)
- **YubiKey**
  - USB/NFC device supporting OTP, U2F
- **RSA SecurID**
  - Time-based OTP authentication token

### Software Solutions
- Password managers
- Encrypted password storage
- Autofill capability
- Password generation and auditing

---

## Smart Card Authentication
Smart card authentication uses a physical card embedded with a microchip to authenticate users securely.

Commonly used in enterprise environments and government systems.

---

## RADIUS (Remote Authentication Dial-In User Service)
RADIUS is a protocol providing centralized Authentication, Authorization, and Accounting (AAA).

Commonly used for:
- VPN connections
- Wireless authentication
- Network access control

### Key Components
- RADIUS client
- RADIUS server
- User database

---

## TACACS+
Terminal Access Controller Access-Control System (TACACS+) is a Cisco-developed AAA protocol.

### Key Features
- Uses TCP (port 49)
- Encrypts entire payload
- Separates authentication, authorization, and accounting

### Components
- TACACS+ client
- TACACS+ server
- User database

---

## OATH (Open Authentication)
OATH is an open standard initiative for authentication.

It supports:
- TOTP (Time-based One-Time Password)
- HOTP (HMAC-based One-Time Password)

Commonly used in authentication apps like Google Authenticator.

---

## Biometric Authentication
Biometric authentication uses unique physical or behavioral traits.

### Examples
- Fingerprint recognition
- Facial recognition
- Iris scan
- Voice recognition
- Behavioral biometrics (typing patterns)

Provides strong identity verification but may raise privacy concerns.

---

## Security Considerations in IAM
- Enforce least privilege
- Implement strong password policies
- Use MFA wherever possible
- Monitor and audit authentication logs
- Protect against credential stuffing and brute-force attacks
