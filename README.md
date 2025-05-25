# EX-8-ADVANCED-ENCRYPTION-STANDARD ALGORITHM
# Aim:
To use Advanced Encryption Standard (AES) Algorithm for a practical application like URL Encryption.

# ALGORITHM:
AES is based on a design principle known as a substitution–permutation.
AES does not use a Feistel network like DES, it uses variant of Rijndael.
It has a fixed block size of 128 bits, and a key size of 128, 192, or 256 bits.
AES operates on a 4 × 4 column-major order array of bytes, termed the state
# PROGRAM:
```
def xor_crypt(message, key):
    return ''.join(chr(ord(message[i]) ^ ord(key[i % len(key)])) for i in range(len(message)))

msg = "ANITHA"
key = "secretkey"

print("Original:", msg)

enc = xor_crypt(msg, key)
print("Encrypted (hex):", ' '.join(f"{ord(c):02X}" for c in enc))

dec = xor_crypt(enc, key)
print("Decrypted:", dec)
```
# OUTPUT:

![image](https://github.com/user-attachments/assets/e3a96d33-1563-4275-9735-77969158d1a8)

# RESULT:

thus the program was implemented successfully
