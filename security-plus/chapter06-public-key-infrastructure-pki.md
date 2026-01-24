# Chapter 6 – Public Key Infrastructure (PKI)

## Introduction to PKI
Public Key Infrastructure (PKI) is a framework that enables secure communication by validating the identity of entities through **digital certificates** and **public key cryptography**.

- A public key is wrapped inside a digital certificate
- Certificates are signed by a trusted **Certificate Authority (CA)**
- Both the sender and the recipient must trust the same CA

---

## Certificate Authorities (CAs)
A Certificate Authority is a trusted entity that issues digital certificates used to verify the identity of individuals, organizations, and systems.

### Roles of Certificate Authorities
- Establish trust on the internet
- Validate identities before issuing certificates
- Define certificate services and policies
- Ensure certificate validity and lifecycle management

### Types of CAs
- **Private CA**: Used internally within organizations
- **Third-party (Public) CA**: Trusted globally (e.g., public internet CAs)

### Types of Certificates Issued
- SSL/TLS certificates
- Code signing certificates
- Email and user certificates

---

## PKI Trust Model (Chain of Trust)
PKI relies on a hierarchical trust structure:

- **Root CA**
  - **Intermediate CA(s)**
    - **Leaf Certificates** (end-entity certificates)

Each level trusts the one above it, forming a secure chain of trust.

---

## Registration and Certificate Signing Requests (CSR)
Before a certificate is issued, a registration and validation process occurs.

### Registration Process
- Submission of required information:
  - Applicant name
  - Organization name
  - Email address
  - Public key (generated during CSR creation)
- CA review
- Approval or rejection

### Certificate Signing Request (CSR)
A CSR is a block of encoded data generated on the server where the certificate will be installed.

#### CSR Components
- **Distinguished Name (DN)**
  - Common Name (CN): Domain name (for SSL certificates)
  - Organization (O)
  - Organizational Unit (OU)
  - Country (C)
- Public key
- Digital signature

---

## Digital Certificates
Digital certificates bind an identity to a public key.

### Certificate Standards
- **X.509 (PKIX)**
- **Public Key Cryptography Standards (PKCS)**

### Certificate Attributes

| Field | Description |
|------|------------|
| Serial Number | Unique identifier assigned by the CA |
| Signature Algorithm | Algorithm used to sign the certificate |
| Issuer | The issuing CA |
| Valid From / To | Certificate validity period |
| Subject | Certificate holder identity (DN) |
| Public Key | Public key and algorithm |
| Extensions | Additional attributes (v3 certificates) |
| Subject Alternative Name (SAN) | Preferred field for DNS names and host identities |

---

## Subject Name Attributes
- **Common Name (CN)**
- **Subject Alternative Name (SAN)**

---

## Certificate Types
- Certificate policies and templates
- Key usage
- Extended/Enhanced key usage
- Critical and non-critical extensions

---

## Web Server Certificate Types
- **Domain Validation (DV)**
  - Verifies domain ownership
- **Extended Validation (EV)**
  - Performs strict identity verification

---

## Other Certificate Types
- **Machine / Computer Certificates**
  - Used by servers and network appliances
  - Identified by FQDN
- **Email / User Certificates**
  - Used for encryption, authentication, and smart card logon
  - Identified by email address
- **Code Signing Certificates**
  - Validate software publisher identity
- **Root Certificates**
  - Self-signed certificates for CAs
- **Self-Signed Certificates**
  - Must be manually trusted

---

## Certificate and Key Management
Proper management is critical to PKI security.

### Key Lifecycle
- Key generation
- Certificate generation
- Secure storage
- Revocation
- Expiration and renewal

Improper key management can introduce serious vulnerabilities.

---

## Certificate Expiration and Renewal
- Certificates have a defined validity period
- Renewal options:
  - Reuse existing key pair
  - Generate a new key pair (re-keying)

### Expiration Handling
- Expired certificates are no longer trusted
- Key material should be archived or securely destroyed
- Secure erasing methods must be used

---

## Certificate Revocation
Certificates may be revoked before expiration.

### Revocation Concepts
- Revocation vs. suspension
- Reason codes

### Certificate Revocation List (CRL)
- List of revoked or suspended certificates
- Browsers and systems check CRLs to verify certificate status

---

## Certificate Pinning
Used to defend against Man-in-the-Middle (MitM) attacks.

- Web servers specify trusted public keys
- Techniques:
  - HTTP Public Key Pinning (HPKP)
  - Certificate Transparency Framework

---

## Certificate Formats
- **DER**
  - Binary format
- **PEM**
  - Base64 encoded ASCII format
- **.CER / .CRT**
  - Can be binary or ASCII
- **PFX / P12 (PKCS #12)**
  - Contains private key (password protected)
- **P7B (PKCS #7)**
  - Used to export certificate chains

---

## OpenSSL
OpenSSL is a widely used open-source library implementing SSL and TLS protocols.

### Common OpenSSL Uses
- Generate private keys
- Create CSRs
- Create self-signed certificates
- Convert certificate formats (PEM ↔ DER)
- Verify certificates
- Check SSL/TLS connections

---

## Common Certificate Issues and Troubleshooting
### Existing Certificates
- Check expiration date
- Verify revocation status

### New Certificates
- Validate key usage and extensions
- Verify subject name and SAN
- Ensure correct chain of trust

### Additional Checks
- System time and date accuracy
- Audit PKI and certificate infrastructure
