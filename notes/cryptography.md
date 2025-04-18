# 🔐 Cryptography

Cryptography is the backbone of secure communication in the digital world. It protects data from unauthorized access and ensures integrity, confidentiality, authentication, and non-repudiation.

## 🔑 Symmetric Key Cryptography

In **symmetric key cryptography**, the same key is used for both encryption and decryption.

- **Speed**: Faster and more efficient for large volumes of data.
- **Common Algorithms**: AES, DES, Blowfish, RC4
- **Use Case**: Encrypting files, databases, and internal communications within a secure network.

🧠 **Example**: Two people share a secret key to send messages—if the key is leaked, so is the entire conversation.

## 🗝️ Asymmetric Key Cryptography

**Asymmetric cryptography** uses a pair of keys: a **public key** to encrypt and a **private key** to decrypt.

- **Security**: More secure for transmitting data over untrusted networks.
- **Common Algorithms**: RSA, ECC, Diffie-Hellman
- **Use Case**: Secure email, SSL/TLS (HTTPS), digital signatures, cryptocurrency wallets.

🔁 **Example**: You share your public key with the world, but only you hold the private key to decrypt the messages sent to you.

## 🧩 Picking the Right Encryption for Different Scenarios

Choosing the correct encryption method depends on:

| Scenario | Recommended Encryption |
|----------|------------------------|
| Large volume file encryption | Symmetric (e.g., AES) |
| Secure online communication | Asymmetric (e.g., SSL/TLS using RSA) |
| Verifying data integrity | Hashing |
| Digital identity verification | Asymmetric (Digital Signatures) |
| Data in motion | Often a combination (e.g., TLS uses asymmetric to exchange a symmetric key) |

✅ **Best Practice**: Use a **hybrid approach**—asymmetric for key exchange and symmetric for data encryption.


## 🧮 Hashing

**Hashing** is a one-way transformation of data into a fixed-size string (hash), commonly used for:

- **Password storage**
- **Data integrity checks**
- **Digital signatures**

🔐 **Properties**:
- Deterministic: Same input = same output
- Irreversible: You can’t get the original data back
- Collision-resistant: Hard to find two inputs with the same hash

**Popular Algorithms**: SHA-256, SHA-3, MD5 (deprecated due to vulnerabilities)

🛡️ **Example**: Hashing a file before sending it allows the recipient to verify its integrity by checking the hash.