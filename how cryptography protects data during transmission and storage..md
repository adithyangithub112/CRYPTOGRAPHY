# **The core objective of cryptography**

## 1. Confidentiality

**Goal:** Ensure that information is **not readable by unauthorized people**.

- Cryptography converts readable data (**plaintext**) into an unreadable form (**ciphertext**).
- Only someone with the correct **key** can convert it back.

**Example:**

When you send a WhatsApp message, even WhatsApp servers cannot read it—only the receiver can.

---

## 2. Integrity

**Goal:** Ensure that data is **not altered** during storage or transmission.

- Cryptographic hashes and message authentication codes detect any modification.
- Even a **1-bit change** in data is detectable.

**Example:**

If someone changes a bank transaction amount during transfer, integrity checks will detect it.

---

## 3. Authentication

**Goal:** Verify the **identity** of the sender or receiver.

- Confirms *who* sent the message.
- Prevents impersonation attacks.

**Example:**

When you log into a website, cryptography proves that:

- You are really *you*
- The website is genuine (not a fake phishing site)

---

## 4. Non-Repudiation

**Goal:** Prevent a sender from **denying** that they performed an action.

- Achieved using digital signatures.
- Legally important in contracts and financial systems.

**Example:**

A person who digitally signs a document cannot later claim:

> “I never signed this.”
> 

---

## 5. Access Control (Supporting Objective)

**Goal:** Ensure **only authorized users** can access specific data or systems.

- Cryptographic keys act as permissions.
- Strong encryption enforces access rules.

# How Cryptography Protects Data During Transmission and Storage

Cryptography is the backbone of modern digital security. It protects data from unauthorized access, tampering, and impersonation while data is **moving across networks (data in transit)** and while it is **stored on devices or servers (data at rest)**.

---

## 1. Protection of Data During Transmission (Data in Transit)

Data in transit refers to information being sent over communication channels such as the internet, Wi-Fi, or mobile networks. These channels are inherently insecure and vulnerable to interception.

### Threats During Transmission

- Eavesdropping (packet sniffing)
- Man-in-the-Middle (MITM) attacks
- Data modification
- Identity spoofing

### Cryptographic Techniques Used

### a) Encryption

- Before transmission, plaintext data is encrypted into ciphertext.
- Even if intercepted, the data is unreadable without the correct key.

Two types are commonly used together:

- **Asymmetric encryption** → for secure key exchange
- **Symmetric encryption** → for fast bulk data encryption

### b) Secure Key Exchange

- Public-key cryptography allows secure sharing of secret keys over insecure networks.
- Once a shared secret is established, symmetric encryption takes over.

### c) Message Integrity & Authentication

- Cryptographic hash functions and MACs ensure data is not altered.
- Digital certificates verify the identity of communicating parties.

### Result

- Confidentiality: attackers cannot read data
- Integrity: tampering is detected
- Authentication: sender and receiver identities are verified

---

## 2. Protection of Data During Storage (Data at Rest)

Data at rest includes files stored on:

- Hard drives
- Databases
- Cloud storage
- Mobile devices

### Threats to Stored Data

- Device theft
- Unauthorized internal access
- Malware
- Data breaches

### Cryptographic Techniques Used

### a) Encryption at Rest

- Data is stored only in encrypted form.
- Decryption occurs only after proper authentication.

Common approaches:

- Full-disk encryption
- File-level encryption
- Database encryption

### b) Key Management

- Encryption keys are stored securely (often in hardware security modules).
- Access to keys is strictly controlled.

### c) Hashing for Password Protection

- Passwords are never stored directly.
- Cryptographic hashes ensure passwords cannot be reversed.

### Result

- Even if storage is compromised, data remains unreadable
- Prevents mass data exposure during breaches

---

## 3. Combined Protection: End-to-End Security

Modern systems combine both protections:

- Data is encrypted **before transmission**
- Remains encrypted **while stored**
- Decrypted only for authorized users

This ensures security throughout the **entire data lifecycle**.

| Security Goal | How Cryptography Achieves It |
| --- | --- |
| Confidentiality | Encryption |
| Integrity | Hash functions, MACs |
| Authentication | Digital signatures, certificates |
| Non-repudiation | Digital signatures |
| Access control | Key-based permissions |
