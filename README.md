---

# Vigenère Cipher

## Overview

The Vigenère Cipher is a method of encrypting alphabetic text by using a simple form of polyalphabetic substitution. Unlike the Caesar Cipher, which shifts all letters by a fixed number of positions, the Vigenère Cipher uses a keyword to determine the shift for each letter in the plaintext.

## How It Works

1. **Key Repetition**: The key is repeated to match the length of the plaintext message. If the key is shorter than the message, it is repeated from the beginning until it matches the length of the message.

2. **Letter Shift**: Each letter in the plaintext is shifted according to the corresponding letter in the key. The shift value is determined by the position of the key letter in the alphabet. For example, if the key letter is 'a', there is no shift; if it's 'b', there's a shift of 1, and so on.

3. **Encryption/Decryption**: To encrypt, each letter in the plaintext is shifted forward by the corresponding shift value. To decrypt, each letter in the ciphertext is shifted backward by the corresponding shift value.

## Example

Suppose we want to encrypt the message "This is a Vigenère cipher!" using the key "watermelon". Here's how the encryption process works:

- Message: "This is a Vigenère cipher!"
- Key: "watermelon"

For each letter in the message, the shift value is determined by the corresponding letter in the key:

1. For the first 'T':
   - Key letter: 'w' (index 22 in the alphabet)
   - Shift: 22
   - Encrypted letter: 'U' (shift 22 positions forward from 'T')

2. For the second 'h':
   - Key letter: 'a' (index 0 in the alphabet)
   - Shift: 0
   - Encrypted letter: 'h' (no shift)

3. Repeat the process for each letter in the message, using the corresponding letter in the key to determine the shift value.

## Usage

To encrypt or decrypt messages using the Vigenère Cipher, provide a message and a key. The key determines the shift value for each letter in the message.

```python
message = "This is a Vigenère cipher!"
key = "watermelon"

# Encryption
encrypted_message = encrypt(message, key)
print("Encrypted message:", encrypted_message)

# Decryption
decrypted_message = decrypt(encrypted_message, key)
print("Decrypted message:", decrypted_message)
```

## Note

- The Vigenère Cipher is more secure than the Caesar Cipher because the shift value varies throughout the message, making it harder to decrypt without knowing the key.
- However, the Vigenère Cipher is still vulnerable to frequency analysis and other cryptanalysis techniques.

---
