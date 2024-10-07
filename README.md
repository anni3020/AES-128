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
