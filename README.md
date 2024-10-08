# AES-128
This project is an implementation of the Advanced Encryption Standard (AES) algorithm, a widely used encryption technique that ensures secure and confidential data transmission. AES is a symmetric key block cipher that operates on 128-bit blocks of data
# AES-128 Encryption Theory

## Introduction
AES-128 is a symmetric encryption algorithm standardized by NIST, and it is widely used to secure digital data. This project explains the theory behind AES-128 encryption and decryption.

## Theory of AES-128
AES-128 uses a 128-bit key to encrypt and decrypt data. It operates as a block cipher, processing data in 128-bit blocks using multiple rounds of substitution, shifting, mixing, and adding a key. Each round is critical to ensuring the security of the data.

- **Symmetric Encryption**: AES-128 uses the same key for both encryption and decryption.
- **Block Cipher**: AES processes data in fixed-size 128-bit blocks.
- **Key Size**: AES-128 has a 128-bit key, which provides strong security.
- **Encryption Process**:
  - **SubBytes**: Non-linear substitution of bytes.
  - **ShiftRows**: Shifting rows cyclically.
  - **MixColumns**: Mixing the columns.
  - **AddRoundKey**: XORing the state with the encryption key.

## Why AES-128?
AES-128 strikes a balance between security and performance, making it a preferred choice for various applications like secure communication, data storage, and online transactions.

## Real-World Applications
AES-128 is used in:
- **Secure messaging apps**
- **VPNs and SSL/TLS protocols**
- **Disk encryption (BitLocker, FileVault)**

## Future Scope
Further exploration of other AES key sizes (192, 256 bits) or different encryption modes (CBC, GCM) can be added to this project.
# Working of AES-128
## AES-128 Encryption Theory

## Introduction
AES-128 is a symmetric key encryption algorithm, standardized by NIST (National Institute of Standards and Technology). It is widely used for secure data transmission in various applications like HTTPS, VPNs, and data encryption at rest.

AES stands for **Advanced Encryption Standard**, and **128** refers to the length of the encryption key (128 bits = 16 bytes). It uses a block cipher technique, where data is encrypted in fixed-size blocks of 128 bits.

## Key Features
- **Symmetric Encryption**: The same key is used for both encryption and decryption.
- **Block Cipher**: Operates on blocks of data, each of 128 bits.
- **Rounds**: AES-128 uses 10 rounds of encryption, with each round consisting of several transformations.

## Steps in AES-128 Encryption

![image](https://github.com/user-attachments/assets/583bab2b-24ec-4fcc-8a9f-9cae1d2c2c02)[](url)
### 1. Key Expansion
AES-128 starts by generating a series of round keys from the original 128-bit key. These round keys are derived using key expansion algorithms and are used during the encryption process.

![key expansion](https://github.com/user-attachments/assets/498c4feb-84de-40b4-8ed4-10e37c52f2ac)[](url)

### 2. Initial AddRoundKey
Before any round of transformation, the input data block (plaintext) is XORed with the first round key. This adds initial confusion to the data, preparing it for further rounds of encryption.

### 3. Main Rounds (9 Rounds)
The next 9 rounds consist of the following steps:

1. **SubBytes (Byte Substitution)**: Each byte in the input block is replaced by a corresponding value from a substitution table called the **S-Box**. This introduces non-linearity in the encryption process.
   
   ![image](https://github.com/user-attachments/assets/16317950-2267-431f-9204-ab27f79edcc4)[](url)
2. **ShiftRows (Row Shifting)**: The rows of the 4x4 matrix representing the 128-bit block are shifted cyclically to introduce diffusion, ensuring that each byte impacts multiple bytes in subsequent rounds.
3. **MixColumns**: Columns of the matrix are mixed using a mathematical transformation that spreads the influence of each byte across the block.
4. **AddRoundKey**: The data block is XORed with the next round key generated in the key expansion step.

### 4. Final Round (10th Round)
The final round omits the **MixColumns** step and only performs the **SubBytes**, **ShiftRows**, and **AddRoundKey** transformations.

## AES-128 Decryption
Decryption is the reverse of encryption. The process involves:
- **Inverse SubBytes**: Replacing each byte with its corresponding inverse from the S-Box.
- **Inverse ShiftRows**: Shifting rows back to their original positions.
- **Inverse MixColumns**: Undoing the column mixing.
- **AddRoundKey**: XORing with the round keys, in reverse order compared to encryption.

## Security of AES-128
AES-128 is considered secure because:
1. **Large Key Space**: With 128-bit keys, there are \(2^{128}\) possible keys, making brute-force attacks impractical.
2. **Complex Rounds**: The combination of SubBytes, ShiftRows, MixColumns, and AddRoundKey provides excellent confusion and diffusion, ensuring high security.

## Applications
AES-128 is used in many security-sensitive areas, including:
- **HTTPS (Secure web communication)**
- **VPNs (Virtual Private Networks)**
- **Encrypted file storage (e.g., BitLocker, FileVault)**
- **Secure messaging applications**

## Conclusion
AES-128 is a highly secure and efficient encryption algorithm that is widely adopted in modern cryptography. Despite the availability of AES-192 and AES-256, AES-128 is often preferred for its balance between performance and security.


