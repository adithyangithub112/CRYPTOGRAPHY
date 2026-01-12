# a. Study of AES (Advanced Encryption Standard)

## Overview

**AES (Advanced Encryption Standard)** is a **symmetric block cipher** adopted as a global encryption standard. It is widely used to secure data in modern systems due to its **high security and efficiency**.

### Block Size

- **Fixed block size:** **128 bits**

### Key Lengths

AES supports three key sizes:

- **128 bits**
- **192 bits**
- **256 bits**

Longer keys provide stronger security but require slightly more computation.

### Number of Rounds

| Key Size | Rounds |
| --- | --- |
| 128-bit | 10 |
| 192-bit | 12 |
| 256-bit | 14 |

### Modes of Operation

AES uses modes to encrypt data larger than one block:

| Mode | Description |
| --- | --- |
| ECB | Simple but insecure (pattern leakage) |
| CBC | Adds chaining, better security |
| CFB | Converts block cipher to stream-like |
| OFB | Stream-oriented mode |
| GCM | Provides encryption + authentication (recommended) |

### Security Strength

- Resistant to brute-force attacks
- No practical attacks known when implemented correctly
- Approved for government and military use

---

# b. Study of DES (Data Encryption Standard)

## Overview

**DES (Data Encryption Standard)** is an older **symmetric block cipher** that was once widely used but is now considered **insecure**.

### Block Size

- **64 bits**

### Key Length

- **64-bit key**, but only **56 bits are effective**
- Remaining 8 bits are parity bits

### Mechanism

DES uses:

- **Feistel structure**
- **16 rounds** of substitution and permutation
- Same algorithm for encryption and decryption (key order reversed)

### Security Limitations

- Small key size makes brute-force attacks feasible
- Vulnerable to modern cryptanalysis
- Broken by dedicated hardware in hours or less

### Current Status

❌ **Not secure**

❌ **Deprecated**

⚠️ Only used for educational purposes

---

# c. Comparison: AES vs DES

| Feature | AES | DES |
| --- | --- | --- |
| Encryption Type | Symmetric block cipher | Symmetric block cipher |
| Block Size | 128 bits | 64 bits |
| Key Length | 128 / 192 / 256 bits | 56 bits (effective) |
| Number of Rounds | 10–14 | 16 |
| Speed | Fast (software & hardware) | Slower |
| Security Strength | Very strong | Weak |
| Resistance to Brute Force | Extremely high | Very low |
| Known Vulnerabilities | None practical | Brute-force attacks |
| Modes Supported | ECB, CBC, CFB, OFB, GCM | ECB, CBC |
| Modern Use | HTTPS, VPNs, disk encryption | None (obsolete) |
| Recommendation | ✅ Strongly recommended | ❌ Not recommended |

## Python-Based AES Encryption Demo

```python
from cryptography.fernet import Fernet

# Generate a secret key
key = Fernet.generate_key()
cipher = Fernet(key)

# Original message
message = b"Secure data using AES encryption"

# Encrypt the message
encrypted_message = cipher.encrypt(message)

# Decrypt the message
decrypted_message = cipher.decrypt(encrypted_message)

print("Original Message:", message)
print("Encrypted Message:", encrypted_message)
print("Decrypted Message:", decrypted_message)

```

> Output:
> 
> 
> Original Message: b'Secure data using AES encryption'
> Encrypted Message: b'gAAAAABpZPUwEEure9Oyj3kni3PXxMFS4BN1mPzwJON0nHDOJ9VDJhAfR2YKY_bpZiEcCqZWd5WLh1zr390NsQj3h2naT_F574Sgw12h5MZIcf1Y5dGJyTCsl1cfMpulC_8tgPpDrY-U'
> Decrypted Message: b'Secure data using AES encryption'
>
