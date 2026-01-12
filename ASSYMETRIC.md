# a. Study of RSA (Rivest–Shamir–Adleman)

## Overview

**RSA** is an **asymmetric (public-key) cryptographic algorithm** used for **secure data transmission, key exchange, and digital signatures**. Its security is based on the **difficulty of factoring large prime numbers**.

---

## 1. RSA Key Generation (Step-by-Step)

1. Choose two large prime numbers:
    
    ```
    p,q
    
    ```
    
2. Compute:
    
    ```
    n = p × q
    
    ```
    
3. Compute Euler’s Totient:
    
    ```
    φ(n) = (p − 1)(q − 1)
    
    ```
    
4. Choose public exponent `e` such that:
    
    ```
    1 < e < φ(n)andgcd(e, φ(n)) =1
    
    ```
    
5. Compute private key `d` such that:
    
    ```
    d × e ≡1 (mod φ(n))
    
    ```
    

### Keys

- **Public key** → (e, n)
- **Private key** → (d, n)

---

## 2. RSA Encryption

```
CiphertextC= P^e mod n

```

Where:

- `P` = plaintext
- `e` = public key exponent
- `n` = modulus

---

## 3. RSA Decryption

```
PlaintextP= C^d mod n

```

Where:

- `d` = private key

---

## 4. Simple RSA Working Diagram

```
Sender                           Receiver
------                           --------
Plaintext (P)
   |
EncryptusingPublicKey (e, n)
   |
Ciphertext (C)  ---------------->  DecryptusingPrivateKey (d, n)
                                      |
                                  Plaintext (P)

```

---

## 5. RSA Characteristics

- Secure but **computationally expensive**
- Requires **large key sizes**
- Slower than symmetric encryption
- Commonly used for **key exchange**, not bulk data

---

# b. Study of ECC (Elliptic Curve Cryptography)

## Overview

**ECC (Elliptic Curve Cryptography)** is an **asymmetric cryptographic technique** based on the mathematics of **elliptic curves over finite fields**. It provides **strong security with much smaller keys**.

---

## 1. Core Concept of ECC

ECC relies on the difficulty of the **Elliptic Curve Discrete Logarithm Problem (ECDLP)**:

> Given points P and Q = kP, finding k is computationally infeasible.
> 

### Elliptic Curve Equation

```
y² = x³ + ax + b

```

---

## 2. ECC Key Generation (Conceptual)

1. Select an elliptic curve and base point `G`
2. Choose a random private key `d`
3. Compute public key:
    
    ```
    Q = d × G
    
    ```
    

### Keys

- **Private key** → d
- **Public key** → Q

---

## 3. ECC Encryption / Key Exchange (Simplified)

ECC is commonly used for:

- **Key exchange (ECDH)**
- **Digital signatures (ECDSA)**

### Simplified ECC Diagram

```
Sender                            Receiver
------                            --------
PrivateKey (dA)PrivateKey (dB)
PublicKey (QA)PublicKey (QB)

Shared Secret:
dA × QB  =  dB × QA

```

Both parties arrive at the **same secret key** without transmitting it.

---

## 4. ECC Characteristics

- Much **smaller keys**
- Faster computation
- Lower power and memory usage
- Ideal for **mobile, IoT, and modern systems**

---

# c. Comparison: RSA vs ECC

| Feature | RSA | ECC |
| --- | --- | --- |
| Cryptography Type | Asymmetric | Asymmetric |
| Mathematical Basis | Integer factorization | Elliptic curve discrete logarithm |
| Key Size (≈ Security) | 2048-bit | 256-bit |
| Security Strength | Strong | Stronger per bit |
| Computational Cost | High | Low |
| Performance | Slower | Faster |
| Memory Usage | High | Low |
| Power Consumption | High | Low |
| Scalability | Moderate | Excellent |
| Best Use Cases | TLS certificates, legacy systems | Mobile, IoT, modern TLS |
| Modern Preference | Declining | Increasing |

---

## Equivalent Security Levels

| RSA Key Size | ECC Key Size |
| --- | --- |
| 1024-bit | 160-bit |
| 2048-bit | 224–256-bit |
| 3072-bit | 256–384-bit |

---

# d. Summary of Working Logic

## RSA Logic (Simplified)

- Security depends on **factoring large numbers**
- Public key encrypts
- Private key decrypts
- Slower but well understood

## ECC Logic (Simplified)

- Security depends on **elliptic curve mathematics**
- Smaller keys, same security
- Faster and efficient
- Better for modern environments
