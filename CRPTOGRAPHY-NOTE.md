# **Cryptography and its Types**

Cryptography is the science of protecting information using mathematical techniques to ensure confidentiality, integrity, and authentication. It transforms readable data into unreadable form, preventing unauthorized access and tampering.

- Converts plaintext into ciphertext using algorithms and keys
- Ensures confidentiality, integrity, authentication, and non-repudiation
- Used in secure communication, digital signatures, passwords, and online transactions
<img width="870" height="428" alt="image" src="https://github.com/user-attachments/assets/5f13a60a-80ee-4843-843c-244c0d08fa3d" />
These algorithms are used for cryptographic key generation, digital signing, and verification to protect data privacy, web browsing on the internet and to protect confidential transactions such as credit card and debit card transactions.

# **Features Of Cryptography**

The features of cryptography that makes it a popular choice in various applications could be listed down as
<img width="800" height="400" alt="image" src="https://github.com/user-attachments/assets/dabb1c78-c9a7-4936-bad2-991ba63ef6f5" />
1. **Confidentiality:** Information can only be accessed by the person for whom it is intended and no other person except him can access it.
2. **Non-repudiation:** The creator/sender of information cannot deny his intention to send information at a later stage.
3. **Integrity:** Information cannot be modified in storage or transition between sender and intended receiver without any addition to information being detected.
4. **Adaptability:** Cryptography continuously evolves to stay ahead of security threats and technological advancements.
5. **Interoperability:** Cryptography allows for secure communication between different systems and platforms.
6. **Authentication:** The identities of the sender and receiver are confirmed. As well destination/origin of the information is confirmed.

# **Working of Cryptography**

As we all know that cryptography technique is use to convert plain text into ciphertext. This technique is done by cryptographic key. Basically cryptographic key is a string of characters which is used to encrypts the data and decrypt the data.
<img width="617" height="278" alt="image" src="https://github.com/user-attachments/assets/61c00998-9761-4a0e-bc02-99295048866d" />
Here,

```
"Hello" is a plaintext and convert into ciphertext "jknnq" with the help of cryptographic key and then decrypt into "Hello".
```

- **Plaintext is created**The original readable message or data.
- **A cryptographic algorithm is chosen**Example: AES, RSA, SHA-256, etc.
- **A key is applied**This key controls how the encryption or hashing is performed.
- **Encryption converts plaintext → ciphertext**The data becomes unreadable to unauthorized users.
- **Ciphertext is transmitted or stored securely**Even if intercepted, it cannot be understood without the correct key.
- **Decryption converts ciphertext → plaintext**The receiver uses the correct key (same key for symmetric, different for asymmetric).
- **Integrity checks may be used**Hashing ensures the message has not been altered.

# **Types Of Cryptography**

There are three types of cryptography, namely Symmetric Key Cryptography, Asymmetric Key Cryptography and Hash functions, here's a detailed explanation below:
<img width="800" height="400" alt="image" src="https://github.com/user-attachments/assets/aaa7b9bd-636d-484a-9eb5-8fe2f4c216fc" />
# **1. Symmetric Key Cryptography**

Symmetric Key Cryptography ****is an encryption system where the sender and receiver of a message use a single common key to encrypt and decrypt messages.

- Symmetric Key cryptography is faster and simpler but the problem is that the sender and receiver have to somehow exchange keys securely.
- The most popular symmetric key cryptography systems are Data Encryption Systems (DES) and Advanced Encryption Systems (AES) .
- <img width="768" height="282" alt="image" src="https://github.com/user-attachments/assets/61017851-ab93-42e8-a063-565feac0a0a8" />

*Symmetric Key Cryptography*

### **Example:**

### **Data Encryption Standard (DES)**

DES (Data encryption standard) is an older encryption algorithm that is used to convert 64-bit plaintext data into 48-bit encrypted ciphertext.

- It uses symmetric keys (which means same key for encryption and decryption).
- It is kind of old by today’s standard but can be used as a basic building block for learning newer encryption algorithms.
- <img width="800" height="400" alt="image" src="https://github.com/user-attachments/assets/f87b56ab-edc2-47ea-b98e-8808b8a89622" />
### **AES (Advanced Encryption Standard):**

AES s a popular encryption algorithm which uses the same key for encryption and decryption.

- It is a symmetric block cipher algorithm with block size of 128 bits, 192 bits or 256 bits.
- AES algorithm is widely regarded as the replacement of DES (Data encryption standard) algorithm.
- <img width="800" height="400" alt="image" src="https://github.com/user-attachments/assets/b2975ccd-27d0-40e8-82ae-4a2cff87dc9a" />

# **2. Hash Functions**

Hash functions do not require a key. Instead, they use mathematical algorithms to convert messages of any arbitrary length into a fixed-length output, known as a hash value or digest.

Hash functions are designed to be one-way, meaning the original input cannot be derived from the output.

Given Below, Some of the most widely used hash functions include:

### **SHA-1:**

- SHA-1 stands for Secure Hash Algorithm 1.
- It is a cryptographic hash function developed by the National Security Agency (NSA) and published by NIST in 1995.
- It was designed to ensure data integrity by converting any input into a fixed-size 160-bit (20-byte) hash value.
- <img width="674" height="504" alt="image" src="https://github.com/user-attachments/assets/b801a103-b360-4ebc-b02a-96fbeccb7456" />
*SHA-1*

**Example of SHA-1 Hash Generator**
<img width="569" height="464" alt="image" src="https://github.com/user-attachments/assets/6d300a49-27bd-4965-a539-c7f539efee60" />
*Example*

### **SHA-256:**

- The SHA-256 algorithm belongs to the family of the SHA 2 algorithms.
- It generates a fixed 256-bit (32-byte) hash value from input data of any length.
- It is widely used in various security applications, including data integrity verification, digital signatures, blockchain technology, and password hashing, due to its strength and resistance to known cryptographic attacks.
- <img width="800" height="400" alt="image" src="https://github.com/user-attachments/assets/ec7545f8-ce26-4240-b060-a811917c16d1" />
*SHA-256*

```
Example:
Data : geeksforgeeks
SHA256 : f8d59362da74ffe833332dc20508f12de6da6a9298c98b3b42873e7298fced78
```

### **MD5:**

- MD5 produces a 128-bit hash value (32-character hexadecimal number) from input data of any size.
- Originally designed for data integrity verification, MD5 was widely used for checksums, digital signatures, and file verification.
- <img width="800" height="400" alt="image" src="https://github.com/user-attachments/assets/d1b2107b-aba9-4758-83bf-0d6c3f6a7b9d" />
<img width="800" height="400" alt="image" src="https://github.com/user-attachments/assets/335e8152-41c2-4235-b0ad-3c80a842a99c" />
*MD5*

### **MD6:**

- MD6 is a cryptographic hash function designed by Ronald Rivest and his team in 2008 as a successor to the MD5 and MD4 algorithms.
- It was created to be highly secure and suitable for modern computing systems, including multi-core processors.
- <img width="800" height="400" alt="image" src="https://github.com/user-attachments/assets/ce0b94a9-d8cb-4a03-b8d6-77ce1c424566" />
*MD6 Hashing*

**Example of MD6 Hash Generator**
<img width="882" height="661" alt="image" src="https://github.com/user-attachments/assets/1502388d-10cf-4572-924d-e1da5d153c90" />
*Example*

# **3. Asymmetric Key Cryptography**

In Asymmetric Key Cryptography a pair of keys is used to encrypt and decrypt information. A sender's public key is used for encryption and a receiver's private key is used for decryption. Public keys and Private keys are different. Even if the public key is known by everyone the intended receiver can only decode it because he holds his private key. The most popular asymmetric key cryptography algorithm is the ****RSA algorithm.
<img width="650" height="325" alt="image" src="https://github.com/user-attachments/assets/63c04237-4bea-4337-89b5-1b72efb7d2b0" />
*Asymmetric Key Cryptography*

### **Examples:**

### **RSA (Rivest-Shamir-Adleman):**

RSA is an basic asymmetric cryptographic algorithm which uses two different keys for encryption. The RSA algorithm works on a block cipher concept that converts plain text into cipher text and vice versa.
<img width="800" height="400" alt="image" src="https://github.com/user-attachments/assets/babc0069-d20a-4dea-b2f8-a9914844f7ff" />
*Encryption in RSA*

**Example:**

```
Choose p = 3 and q = 11
Compute n = p * q = 3 * 11 = 33
This n is part of the public key and also used in both encryption and decryption
Computer Euler's function φ(n)
ϕ(n)=(p−1)(q−1)=(3−1)(11−1)=2×10=20
Choose e such that 1 < e < φ(n) and e and φ (n) are coprime. Let e = 7
Compute a value for d such that (d * e) % φ(n) = 1. One solution is d = 3 [(3 * 7) % 20 = 1]
Public key is (e, n) = (7, 33)
Private key is (d, n) = (3, 33)

Encyption:
Let’s say the message M=4 (must be < n)
Ciphertext C=M^e modn=4^3 mod33=64 mod33=31
Encrypted Message = 31

Decryption:
M=C^d modn=31^7 mod33
Use modular Exponential
31^2 = 961 mod33=431^4 = (31^2)^2 = 1631^7 = 31.31^2.31^4 = 31.4.16 = 1984 mod 33Now, 1984 mod 33 = 4Decrypted Message= 4
```

- 31^2 = 961 mod33=4
- 31^4 = (31^2)^2 = 16
- 31^7 = 31.31^2.31^4 = 31.4.16 = 1984 mod 33

# **ECC (Elliptic Curve Cryptography):**

lliptic Curve Cryptography (ECC) is a type of asymmetric encryption that provides strong security with smaller keys than RSA. It’s efficient, fast, and ideal for devices with limited resources like smartphones, IoT devices, and blockchain wallets. ECC is widely used in secure communications such as TLS/SSL and cryptocurrencies due to its lightweight yet powerful encryption.
<img width="658" height="400" alt="image" src="https://github.com/user-attachments/assets/39bfebf1-d89c-449d-ae48-ef4728015155" />
*Elliptic Curve*

**Equation:**

```
We use the standard elliptic curve equation: y^2 = x^3 + ax + b mod p
Let's choose:
Prime field: p =23Curve parameters: a = 1, b = 1So the curve becomes: y^2 = x^3 + x + 1 mod 23
```

- Prime field: p =23
- Curve parameters: a = 1, b = 1

# Applications of Cryptography

Cryptography has wide area of applications in the modern world, where the technology is rapidly evolving. These are some of the most common applications of cryptography listed below:
<img width="800" height="400" alt="image" src="https://github.com/user-attachments/assets/ce39c4fd-be1c-41c4-ae18-7e8bd02f553c" />
*Applications*

**1. Password Security**: Passwords are hashed before storage to prevent exposure even if the database is leaked.

**2. Digital Currencies**: Bitcoin and other cryptocurrencies use cryptography for transaction integrity and identity protection.

**3. Secure Web Browsing (HTTPS)**: SSL/TLS protocols encrypt communication between browser and server.

**4. Electronic Signatures:** Legally valid digital signatures created using public-key cryptography.

**5. Authentication Systems**: Used in bank logins, secure networks, and access control systems.

**6. End-to-End Encryption**: Messaging apps like WhatsApp and Signal ensure only intended users read the messages.

# **Classical Ciphers**

Ciphers are methods used to transform readable data (plaintext) into unreadable data (ciphertext) so that only authorized parties can understand the original content.
<img width="800" height="400" alt="image" src="https://github.com/user-attachments/assets/ada9db9e-3037-43a6-ad02-905aec386cf0" />
*Cipher*

**Examples**

- Military/Spying - Early secret communication (e.g., Enigma machine)
- CTFs / Hack Challenges - Puzzles often hide flags using classical ciphers
- Legacy malware - Obfuscates payloads using simple XOR or Caesar ciphers

### **Categories of Ciphers:**

There are mainly two types of Classical Ciphers

**1. Substitution Ciphers**: Replace characters with other characters using a defined rule

**Example**:

```
In Caesar Cipher, A → D, B → E, etc.
```

**Real-Life Use**: Simple password obfuscation, CTFs, and puzzle challenges.

**2. Transposition Ciphers:** Rearrange the order of characters without changing them.

**Example:**

Rail Fence Cipher, where characters are written in a zigzag and read row by row.

**Real-Life Use:** Basic message encoding to confuse readers.

### **Types of Classical Ciphers**

There are basic types of Classical Ciphers.

| **Cipher Name** | **Description** | **Real-life/CTF Use** |
| --- | --- | --- |
| **Caesar Cipher** | Each letter is shifted a fixed number of places. | Hidden messages in simple malware, games, or emails. |
| **Vigenère Cipher** | Uses a keyword to shift letters; more secure than Caesar. | Used in older secret messages and CTF puzzles. |
| **Atbash Cipher** | A → Z, B → Y… Reverses the alphabet. | Often seen in basic stego/crypto challenges. |
| **ROT13** | A Caesar Cipher with a shift of 13. | Used in hiding spoilers or light obfuscation online. |
| **Rail Fence Cipher** | A form of transposition cipher that rearranges the order. | Great for simple puzzles and password hiding.
 |

# **Steganography**

Steganography is the practice of concealing information. It involves hiding data within an ordinary, non-secret file or message to prevent detection. The hidden information is being extracted at the receiving end. Often, steganography is combined with encryption to add an extra layer of security for the hidden data. With the help of Steganography, we can hide any digital content virtually like text, image, videotape, etc.

# **Common Types of Steganography:**

Here are the types mentioned below about Steganography

### **Image Stego (LSB)**

- Data is hidden in the least significant bits of pixels.
- **Real-Life Use**: Malware communication, CTF challenges.

### **Text Stego**

- Secret data hidden using invisible characters, spaces, or misspelled words.
- **Real-Life Use:** Covert communication in censored countries.

### **Audio Stego**

- Hidden messages embedded in audio signals, often inaudible.
- **Real-Life Use:** Watermarking or espionage.

### **Video Stego**

- Embeds information in video frames or metadata.
- **Real-Life Use:** Covert data exfiltration techniques.

### **Metadata Stego**

- Stores data in metadata fields (e.g., EXIF data in images).
- **Real-Life Use:** Hiding payload links in innocent-looking files.

![steno](https://media.geeksforgeeks.org/wp-content/uploads/20250806153726981270/steno.webp)

*Steganography*

# **Tools for Stego Practice:**

Here are the basic tool of Steganography

| **Tool** | **Use** |
| --- | --- |
| **Steghide** | Hide/extract data from images/audio |
| **zsteg** | Analyze PNG/BMP for hidden messages |
| **ExifTool** | Extract hidden metadata in images |
| **binwalk** | Extract hidden content in binaries |
| **strings** | Find readable data inside files |
| **stegsolve.jar** | GUI tool to analyze and dissect images |

# **Hands-On Practice**

Lets try ciphering a phrase and how it works.

- User CyberChef to encode the plaintext, and use correct operations to Encode/Decode Cipher.
- Types Cipher> Drag Caesar Cipher box into Recipe > Type "Hello Friends" in Input field > Change Box height
- You will notice that the output will change as you change the box height, but at a point you will be able to view the phrase Hello friends in the output box again.

![hlw_f1.webp](https://media.geeksforgeeks.org/wp-content/uploads/20250806155925829357/hlw_f1.webp)
