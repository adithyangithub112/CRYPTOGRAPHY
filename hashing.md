## a. Hashing Process and Its Role in Ensuring Data Integrity

### What Is Hashing?

**Hashing** is the process of converting input data of any size (message, file, or password) into a **fixed-length value** called a **hash** or **message digest**, using a mathematical algorithm.

### Hashing Process (Step-by-Step)

1. Input data (file/message/password) is given to a hash algorithm
2. The algorithm processes the data using mathematical operations
3. A fixed-length hash value is produced
4. The hash uniquely represents the original data

### Role in Data Integrity

Hashing ensures **data integrity** by allowing detection of any unauthorized modification.

- If data changes → hash changes
- Even a **single-bit change** produces a completely different hash
- By comparing original and received hashes, integrity can be verified

### Real-World Integrity Use

- File downloads (checksum verification)
- Software updates
- Digital signatures
- Database integrity checks

---

## b. Popular Hashing Algorithms

### 1. MD5 (Message Digest Algorithm 5)

**Key Features**

- Produces a 128-bit hash value
- Fast computation

**Limitations**

- Vulnerable to collisions
- No longer considered secure

**Current Status**

❌ **Not recommended for security purposes**

✅ Still used for non-security checks (e.g., file comparison)

---

### 2. SHA-1 (Secure Hash Algorithm 1)

**Key Features**

- Produces a 160-bit hash value
- More secure than MD5

**Limitations**

- Collision attacks have been demonstrated
- Considered weak by modern standards

**Current Status**

❌ **Deprecated for security use**

---

### 3. SHA-256 (Secure Hash Algorithm 256)

**Key Features**

- Part of the SHA-2 family
- Produces a 256-bit hash value
- Extremely low collision probability

**Advantages**

- Strong security
- Widely adopted
- Resistant to known practical attacks

**Current Status**

✅ **Recommended and widely used**

---

### Comparison of Hashing Algorithms

| Algorithm | Hash Length | Security Status | Common Use Today |
| --- | --- | --- | --- |
| MD5 | 128-bit | Broken | Non-security checks |
| SHA-1 | 160-bit | Weak | Legacy systems |
| SHA-256 | 256-bit | Secure | Integrity, digital signatures, blockchain |

---

## c. Collision Resistance and Its Importance

### What Is a Collision?

A **collision** occurs when **two different inputs produce the same hash value**.

```
InputA ≠InputB
But
Hash(A)=Hash(B)

```

### Collision Resistance

**Collision resistance** is a property of a hash function that makes it **computationally infeasible** to find two different inputs with the same hash.

### Why Collision Resistance Is Important

1. **Maintains Trust**
    - Prevents attackers from substituting malicious data with the same hash
2. **Protects Digital Signatures**
    - If collisions exist, fake documents can appear authentic
3. **Ensures File Integrity**
    - Prevents tampered files from passing integrity checks
4. **Prevents Security Exploits**
    - Weak collision resistance enables impersonation and fraud

### Real-World Impact

- MD5 and SHA-1 failed due to poor collision resistance
- SHA-256 remains secure because collisions are practically impossible

---

## Final Summary

- **Hashing** converts data into a fixed-length digest for integrity verification
- **MD5 and SHA-1** are no longer secure due to collision vulnerabilities
- **SHA-256** is currently secure and widely used
- **Collision resistance** is critical to prevent data forgery and ensure trust

> Hashing does not hide data—it protects its integrity.
>
