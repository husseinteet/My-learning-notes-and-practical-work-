# Chapter 5 – Cryptography & Cryptographic Concepts

## Introduction to Cryptography
Cryptography is the field of securing information and communications using mathematical techniques to protect data from unauthorized access, tampering, or disclosure.

---

## Encryption and Decryption
- **Encryption**: The process of converting plaintext into ciphertext using an algorithm and a key
- **Decryption**: The reverse process of converting ciphertext back into plaintext

### Key Terminology
- **Plaintext**: The original readable message
- **Ciphertext**: The encrypted, unreadable message
- **Cipher**: The algorithm used for encryption and decryption
- **Cryptanalysis**: The study of breaking cryptographic systems

---

## Hash Algorithms
Hash algorithms convert input data of any size into a fixed-size output and are **one-way functions**.

### Common Hashing Algorithms
#### MD5 (Message Digest 5)
- Output size: 128 bits (16 bytes)
- Uses: Checksums and data integrity verification
- Security: Weak due to collision vulnerabilities

#### SHA-1 (Secure Hash Algorithm 1)
- Output size: 160 bits (20 bytes)
- Previously used for certificates and digital signatures
- Security: Vulnerable to collision attacks (not recommended)

#### SHA-2
- Variants: SHA-224, SHA-256, SHA-384, SHA-512
- Widely used in modern security applications
- Designed to resist known cryptographic attacks

#### SHA-3
- Output sizes: 224, 256, 384, 512 bits
- Newer standard and alternative to SHA-2
- Strong resistance against cryptographic attacks

---

## Encryption Ciphers and Keys
- Hashing is **not encryption** (not reversible)
- Encryption is a reversible process using a secret key
- Security relies on key secrecy, not algorithm secrecy

### Types of Keys
- **Symmetric key**: Same key for encryption and decryption
- **Asymmetric key**: Public key for encryption, private key for decryption

---

## Symmetric Encryption
- Uses a single shared key
- Fast and efficient
- Key distribution is a major challenge
- Provides confidentiality only

### Examples
- **AES**
  - Key sizes: 128, 192, 256 bits
  - Widely used in government and commercial systems
- **DES**
  - Key size: 56 bits
  - Considered insecure
- **3DES**
  - Applies DES three times
  - More secure than DES but still deprecated

---

## Asymmetric Encryption
- Uses public/private key pairs
- Suitable for authentication and key exchange
- Not efficient for large data sizes

### Examples
- **RSA**
  - Typical key size: 2048 bits or higher
  - Used for secure communication and digital signatures
- **ECC (Elliptic Curve Cryptography)**
  - Smaller keys with equivalent security
  - Efficient for mobile and low-power devices

---

## Stream and Block Ciphers
### Stream Ciphers
- Encrypt data bit-by-bit or byte-by-byte
- Examples:
  - RC4 (deprecated)
  - ChaCha20 (modern and secure)

### Block Ciphers
- Encrypt fixed-size blocks (usually 128 bits)
- Examples:
  - AES
  - Blowfish
  - Twofish

### Key Length
- Longer keys provide stronger security
- Proper key management is critical

---

## Public Key Cryptography
Enables secure communication over insecure networks.

### Algorithms
- **RSA**
- **DSA**
- **ElGamal**
- **Diffie-Hellman**
- **Post-Quantum Cryptography**

---

## Digital Signatures
- Verify authenticity and integrity
- Provide non-repudiation
- Use hashing and public key cryptography

### Common Types
- RSA-based signatures
- DSA
- ECC-based signatures

---

## Digital Envelope
A hybrid approach combining:
- Symmetric encryption for data
- Asymmetric encryption for key exchange

---

## Digital Certificates
Electronic credentials that verify identities in digital communications.

### Certificate Contents
- Public key
- Identity information
- Certificate Authority (CA) details
- Validity period
- CA digital signature

---

## Cipher Suites and Modes of Operation
### Cipher Suite Components
- Signature algorithm
- Key exchange algorithm
- Bulk encryption algorithm

### Modes of Operation
- Define how block ciphers encrypt large data streams
- Example modes: CBC, GCM, CTR

---

## Authenticated Encryption
Provides:
- Confidentiality
- Integrity
- Authenticity

### AE and AEAD
- **AE**: Encryption + authentication
- **AEAD**: Allows additional authenticated but unencrypted data

---

## Authentication
The process of verifying identity.

### Methods
- Password-based
- PKI
- Two-Factor Authentication (2FA)
- Biometrics

---

## Non-Repudiation
Prevents denial of actions or messages.

### Techniques
- Digital signatures
- Timestamping
- Secure audit trails

---

## Hybrid Encryption
- Asymmetric encryption secures symmetric keys
- Symmetric encryption secures bulk data
- Used in TLS and VPNs

---

## Cryptographic Protocols
### Confidentiality
- TLS
- VPN

### Integrity and Resiliency
- Hash functions
- Message Authentication Codes (MACs)
- Secure control messaging

---

## Performance Limitations
- Speed
- Latency
- Key size overhead
- Computational complexity

---

## Attacks on Cryptography
### Man-in-the-Middle (MITM)
- Intercepts communication
- Can alter public keys

### Downgrade Attacks
- Forces use of weaker protocols or ciphers

---

## Key Stretching and Salting
### Key Stretching
- Adds computational cost
- Slows brute-force attacks

### Salting
- Adds random data before hashing
- Prevents rainbow table attacks
