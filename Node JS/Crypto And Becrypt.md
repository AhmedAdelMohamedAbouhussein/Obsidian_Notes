**encryption/decryption** using Node.js `crypto` module, and also **password hashing** with `bcrypt`.

![[Pasted image 20250816184310.png]]
- `algorithm` → defines which encryption algorithm to use, e.g., `'aes-256-cbc'`.
- `ENCRYPTION_KEY` → a 32-byte key in hexadecimal format. Used to encrypt/decrypt.
- `IV_LENGTH` → Initialization Vector length, required for some algorithms to ensure encryption is randomized.

![[Pasted image 20250816184320.png]]
1. Checks if `text` is empty.
2. Generates a **random IV** (initialization vector) for extra security.
3. Creates a cipher using the chosen algorithm, key, and IV.
4. Encrypts the text:
    - `cipher.update(text, 'utf8', 'hex')` converts plaintext (utf8) to encrypted hex.
    - `cipher.final('hex')` finalizes encryption.
5. Returns the IV and encrypted text combined with `:` (so it can be decrypted later).
> **IV is needed for decryption**, so it’s stored alongside the ciphertext.

![[Pasted image 20250816184412.png]]
1. Splits the stored string to get `iv` and `encryptedText`.
2. Converts `iv` back to a Buffer.
3. Creates a decipher using the same algorithm, key, and IV.
4. Decrypts the text back to plaintext.
✅ This allows you to **encrypt sensitive data** (like a secret note) and decrypt it later securely.


password hashibg
![[Pasted image 20250816184452.png]]
- **Pre-save hook**: runs before saving a user.
- Only hashes password if it’s **new or modified**.
- `bcrypt.genSalt(saltRounds)` → generates a random salt.
- `bcrypt.hash(password, salt)` → hashes the password + salt for security.


comparing password
![[Pasted image 20250816184525.png]]
- Compares the plain password entered by a user with the hashed password in DB.
- Returns **true/false** asynchronously.


### **Summary**
- **crypto.encrypt / crypto.decrypt** → use for reversible encryption of sensitive data.
- **bcrypt.hash / comparePassword** → use for secure **password storage**, which cannot be decrypted.

🔹 **Important**:
- Never store actual passwords. Only store bcrypt hashes.
- Use crypto for things that need to be decrypted later (like API keys, secret tokens).