## 1. Introduction to GnuPG

**GnuPG (GNU Privacy Guard)**, commonly abbreviated as **GPG**, is a **free and open-source implementation of the OpenPGP standard**.  
It is used to **secure data and communications** by providing:

- **Encryption** (confidentiality)
- **Digital signatures** (authentication & integrity)
- **Key management**

GnuPG is widely used for:

- Secure email communication
- File encryption
- Software package verification
- Secure backups
- Authentication in systems like Git

---

## 2. Why GnuPG Is Important

GnuPG helps solve major security problems:

|Problem|Solution Provided by GnuPG|
|---|---|
|Unauthorized data access|Encryption|
|Message tampering|Digital signatures|
|Identity impersonation|Public-key verification|
|Secure file sharing|Asymmetric cryptography|

It is trusted because:

- Open-source (auditable)
- Strong cryptography
- Cross-platform (Linux, Windows, macOS)

---

## 3. Cryptography Basics Used in GnuPG

### 3.1 Symmetric Encryption

- Same key used for encryption and decryption
- Fast but key distribution is difficult

Example algorithms:

- AES
- CAST5

---

### 3.2 Asymmetric Encryption (Public-Key Cryptography)

GnuPG mainly relies on **asymmetric cryptography**.

Each user has:

- **Public Key** → Shared with others
- **Private Key** → Kept secret

|Key Type|Purpose|
|---|---|
|Public Key|Encrypt data, verify signatures|
|Private Key|Decrypt data, create signatures|

Common algorithms:

- RSA
- ECC (Elliptic Curve Cryptography)
- DSA

---

### 3.3 Hybrid Encryption (How GnuPG Actually Works)

GnuPG combines both methods:

1. Generates a **random symmetric session key**
2. Encrypts data with the session key
3. Encrypts the session key using the recipient’s **public key**

This gives:

- Speed (symmetric)
- Security (asymmetric)

---

## 4. Key Concepts in GnuPG

### 4.1 Key Pair

A **key pair** consists of:

- Public key
- Private key

Keys include metadata:

- User name
- Email
- Expiration date
- Key ID and fingerprint

---

### 4.2 Key Fingerprint

- A **unique hash** of a public key
- Used to verify authenticity
- Prevents man-in-the-middle attacks

Example:

`ABCD 1234 EFGH 5678 IJKL 9012 MNOP 3456 QRST 7890`

---

### 4.3 Keyring

- A local database storing keys
    
- Types:
    - Public keyring
    - Private keyring

---

## 5. Installing GnuPG

### Linux

`sudo pacman -S gnupg 
`sudo apt install gnupg`

### Windows

`Install Gpg4win`

### macOS

`brew install gnupg`

---

## 6. Generating a GPG Key Pair

`gpg --full-generate-key`

Steps include:

1. Select key type (RSA recommended)
2. Choose key size (2048 / 4096 bits)
3. Set expiration
4. Enter user name and email
5. Set a strong passphrase

---

## 7. Encrypting and Decrypting Files

### Encrypt a File

`gpg -e file.txt`

or specify a recipient:

`gpg -e -r user@email.com file.txt`

Result:

`file.txt.gpg`

---

### Decrypt a File

`gpg -d file.txt.gpg`

---

## 8. Digital Signatures in GnuPG

### Purpose of Digital Signatures

- Verify sender identity
- Ensure data integrity
- Prevent repudiation

---

### Sign a File

`gpg --sign file.txt`

---

### Verify a Signature

`gpg --verify file.txt.gpg`

---

### Detached Signatures (Common for Software)

`gpg --detach-sign file.txt`

Produces:

`file.txt.sig`

---

## 9. Importing and Exporting Keys

### Export Public Key

`gpg --export -a user@email.com > publickey.asc`

---

### Import a Key

`gpg --import publickey.asc`

---

## 10. Trust Model in GnuPG (Web of Trust)

GnuPG does **not rely on a central authority**.

Instead:

- Users sign each other’s keys
- Trust is built through verification

Trust levels:

- Unknown    
- Marginal
- Full
- Ultimate

---

## 11. Common Use Cases of GnuPG

- 🔐 Encrypting sensitive files
- 📧 Secure email (with Thunderbird, Enigmail)
- 🧾 Signing Git commits
- 📦 Verifying Linux packages
- 💾 Encrypted backups

---

## 12. Advantages of GnuPG

✔ Free and open-source  
✔ Strong cryptography  
✔ Cross-platform  
✔ Industry standard  
✔ Highly customizable

---

## 13. Limitations of GnuPG

✖ Complex for beginners  
✖ Manual key management  
✖ Misconfiguration can reduce security

---

## 14. Summary

GnuPG is a **powerful cryptographic tool** that provides:

- Secure communication
- Data protection
- Identity verification
    

It plays a critical role in:

- Linux systems
- Secure development workflows
- Privacy-focused communication