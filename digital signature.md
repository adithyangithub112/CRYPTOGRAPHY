# a. Digital Signatures — Definition and Purpose

## What Are Digital Signatures?

A **digital signature** is a **cryptographic mechanism** that proves:

- **Who** sent a message or document
- **That the message has not been altered**
- **That the sender cannot deny sending it**

Digital signatures are the digital equivalent of handwritten signatures, but they are **far more secure** because they rely on cryptography.

---

## Core Purposes of Digital Signatures

### 1. Authenticity

Ensures that the message truly comes from the claimed sender.

- Verifies the sender’s identity
- Prevents impersonation

### 2. Integrity

Ensures that the message has **not been modified** after signing.

- Any change in data invalidates the signature

### 3. Non-Repudiation

Ensures that the sender **cannot deny** having signed the message.

- Provides legal and forensic proof of origin

---

# b. How Digital Signatures Use Hashing and Asymmetric Encryption

Digital signatures combine **two cryptographic techniques**:

### 1. Hashing

- Converts the message into a **fixed-length hash**
- Even a tiny change in the message produces a different hash
- Ensures integrity

### 2. Asymmetric Encryption

- Uses a **private key** to sign
- Uses a **public key** to verify
- Ensures authenticity and non-repudiation

🔑 **Important Note:**

The message itself is **not encrypted** in a digital signature—only the **hash** is signed.

---

# c. Digital Signature Process (Step-by-Step)

## Signing Process (Sender Side)

1. Original message is created
2. A **hash** of the message is generated
3. The hash is **encrypted using the sender’s private key**
4. The encrypted hash becomes the **digital signature**
5. Message + digital signature are sent together

### Signing Logic (Simplified)

```
Message →Hash →EncryptwithPrivateKey →DigitalSignature

```

---

## Verification Process (Receiver Side)

1. Receiver receives message and digital signature
2. Receiver hashes the received message
3. Receiver decrypts the signature using the **sender’s public key**
4. Both hashes are compared
- If hashes match → ✅ signature valid
- If hashes differ → ❌ message altered or sender invalid

### Verification Logic (Simplified)

```
ReceivedMessage →Hash
DigitalSignature →DecryptwithPublicKey →Hash
CompareHashes →Verify

```

---

## Why This Process Is Secure

| Property | How It Is Achieved |
| --- | --- |
| Authenticity | Only sender has the private key |
| Integrity | Hash changes if message changes |
| Non-repudiation | Sender cannot deny private key usage |

---

# d. Real-World Applications of Digital Signatures

## 1. Software Signing

**Purpose**

- Ensures software is genuine
- Prevents malware injection

**How it works**

- Software developers digitally sign applications
- Operating systems verify the signature before installation

**Real-world examples**

- Microsoft Windows code signing
- Mobile app stores verifying developer signatures

---

## 2. Email Verification

**Purpose**

- Confirms email sender identity
- Prevents email tampering

**How it works**

- Emails are signed using digital signature standards
- Receiver verifies sender authenticity

**Technologies**

- PGP, S/MIME

**Use cases**

- Secure corporate communication
- Government and legal correspondence

---

## 3. Legal and Official Documents

**Purpose**

- Legally binding electronic signatures
- Proof of agreement and consent

**How it works**

- Documents are signed digitally using certified keys
- Signature proves signer identity and document integrity

**Use cases**

- Online contracts
- Government forms
- Financial agreements

---

## Final Summary

- **Digital signatures** ensure **authenticity, integrity, and non-repudiation**
- They work by **hashing a message and encrypting the hash with a private key**
- Verification is done using the **public key**
- Widely used in **software security, email systems, and legal documentation**

> Encryption hides data, hashing checks data, and digital signatures prove trust.
>
