# 🔓 Password Cracking Lab

This project demonstrates the process of password cracking using hashing algorithms and dictionary attacks — a critical component of cybersecurity learning.

## 🧠 Objectives

- Understand how password hashing works (MD5, SHA1, SHA256)
- Practice cracking password hashes using common and custom wordlists
- Learn how tools like `John the Ripper`, `CUpp`, and `Hash-Identifier` are used
- Respect data privacy and responsibly sanitize sensitive outputs

---

## 🛠️ Tools Used

- **John the Ripper** – for brute-force and dictionary attacks
- **rockyou.txt** – default wordlist for testing common passwords
- **CUpp (Common User Passwords Profiler)** – to generate custom wordlists
- **Hash-Identifier / hashid** – to detect hashing algorithms
- **Kali Linux** – used as the primary pentesting environment

---

## 🧪 Lab Structure

### 🔐 1. Hash Creation

Hashes were created using:
```bash
echo -n "hacker" | md5sum
echo -n "xijinping" | sha1sum
echo -n "ramdhan12" | sha256sum

