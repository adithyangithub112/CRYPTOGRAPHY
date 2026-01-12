# Differentiate Between Encryption, Encoding, and Hashing

## a. Encryption

**Encryption** is the process of transforming readable data (**plaintext**) into an unreadable format (**ciphertext**) using a **cryptographic algorithm and a secret key**. The main goal of encryption is to **protect data confidentiality** so that only authorized users can access the information.

Encryption is **reversible**, but only by someone who possesses the correct **decryption key**.

**Key points**

- Provides confidentiality
- Requires a key
- Used for data in transit and data at rest

**Examples**

- AES for file and disk encryption
- RSA for secure key exchange

---

## b. Encoding

**Encoding** is the process of converting data from one format to another to ensure **safe transmission, storage, or system compatibility**. It is **not a security mechanism** and does not use keys. Anyone who knows the encoding scheme can easily decode the data back to its original form.

**Key points**

- Focuses on data representation, not security
- Easily reversible
- Used to handle data format limitations

**Examples**

- Base64 for email attachments
- URL encoding for web data

---

## c. Hashing

**Hashing** is a **one-way cryptographic transformation** that converts data into a fixed-length output called a **hash value** or **digest**. It is designed so that the original data **cannot be recovered** from the hash. Hashing is mainly used to ensure **data integrity** and for **secure password storage**.

**Key points**

- One-way process (irreversible)
- Small input change produces a large hash change
- No key required (in basic hashing)

**Examples**

- SHA-256 for integrity checks
- bcrypt for password hashing

---

## d. Comparison Table: Encryption vs Encoding vs Hashing

| Feature | Encryption | Encoding | Hashing |
| --- | --- | --- | --- |
| **Primary Purpose** | Protect data from unauthorized access | Make data suitable for transmission or storage | Verify data integrity and authenticity |
| **Security Function** | Yes (confidentiality) | No (formatting only) | Yes (integrity, authentication) |
| **Uses a Key** | Yes | No | No |
| **Reversibility** | Reversible with the correct key | Easily reversible | Irreversible (one-way) |
| **Output Length** | Variable | Variable | Fixed length |
| **Effect of Small Input Change** | Predictable | Predictable | Large, unpredictable change |
| **Common Use Cases** | HTTPS, VPNs, disk encryption | Base64 in emails, URL encoding | Password storage, file integrity checks |
| **Example Algorithms** | AES, RSA | Base64, ASCII | SHA-256, bcrypt |
