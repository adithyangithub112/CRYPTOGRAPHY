## a. Block Ciphers

### Definition

A **block cipher** is an encryption technique that encrypts data in **fixed-size blocks** (for example, 64-bit or 128-bit blocks) using the **same secret key**. Each block of plaintext is processed as a unit to produce a block of ciphertext.

### Key Characteristics

- Operates on **fixed-size blocks**
- Uses **modes of operation** to handle large data
- Strong security when properly implemented

### Examples

- **AES (Advanced Encryption Standard)** – 128-bit block size
- **DES (Data Encryption Standard)** – 64-bit block size (now considered insecure)

### Simple Logic Illustration (Block Cipher)

```
PlaintextBlocks:
[P1][P2][P3]

EncryptionwithKeyK:
[P1]--K-->[C1]
[P2]--K-->[C2]
[P3]--K-->[C3]

Ciphertext:
[C1][C2][C3]

```

Each plaintext block is encrypted separately (or chained, depending on mode).

---

## b. Stream Ciphers

### Definition

A **stream cipher** encrypts data **one bit or one byte at a time** by combining the plaintext with a **keystream** generated from a secret key.

### Key Characteristics

- No fixed block size
- Encryption happens continuously
- Very fast and efficient for real-time data

### Examples

- RC4 (now deprecated)
- Modern stream-based designs used in wireless and mobile communication

### Simple Logic Illustration (Stream Cipher)

```
Plaintext Stream:P1P2P3P4
Keystream:K1K2K3K4
⊕⊕⊕⊕

Ciphertext:C1C2C3C4

```

Each bit/byte of plaintext is encrypted immediately as data flows.

---

## c. Comparison: Block Cipher vs Stream Cipher

| Feature | Block Cipher | Stream Cipher |
| --- | --- | --- |
| **Data Processing** | Fixed-size blocks | Bit-by-bit or byte-by-byte |
| **Speed** | Slower than stream ciphers | Faster for real-time data |
| **Memory Usage** | Higher | Lower |
| **Latency** | Higher (waits for full block) | Very low |
| **Error Propagation** | Errors may affect an entire block | Errors usually affect only one bit/byte |
| **Security Level** | Very strong when using secure modes | Strong, but depends heavily on keystream design |
| **Flexibility** | Less flexible | Highly flexible |
| **Modes Required** | Yes (ECB, CBC, GCM, etc.) | No modes required |
| **Best Use Cases** | File encryption, disk encryption, databases | Streaming data, voice, video, wireless communication |
| **Implementation Complexity** | Moderate to high | Lower |

---

## d. Security and Use-Case Summary

### Block Ciphers

- Highly secure when used with modern algorithms and modes
- Suitable for **large data storage**
- Vulnerable if used with weak modes or outdated algorithms

### Stream Ciphers

- Excellent for **real-time communication**
- Low latency and fast encryption
- Reusing keystreams can cause serious security failures
