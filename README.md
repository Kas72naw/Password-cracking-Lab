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
🗂 2. Cracking with Public Wordlist
Ran John with rockyou.txt for MD5 & SHA1:

bash
Copy
Edit
john --format=raw-md5 --wordlist=/usr/share/wordlists/rockyou.txt md5.hash
john --format=raw-sha1 --wordlist=/usr/share/wordlists/rockyou.txt sha1.hash
✅ Successfully cracked both.

⚙️ 3. Cracking SHA256 with Custom Wordlist
SHA256 could not be cracked with rockyou.txt, so a custom wordlist was made using:

bash
Copy
Edit
cupp -i
Tried again:

bash
Copy
Edit
john --format=raw-sha256 --wordlist=custom.txt sha256.hash
❌ No success — great for showing real-world limitations.

🧾 Files Included
md5.hash, sha1.hash, sha256.hash — sample hash files

lab.txt, ramdhan.txt, xi.txt, kalisimple.txt — custom/generated wordlists

*.png — screenshots of terminal outputs

README.md — documentation (this file)

📚 What I Learned
The importance of strong password policies

How tools like john and cupp operate

Hash formats and their weaknesses

Ethical responsibility to sanitize sensitive data (like live host IPs)

⚠️ Disclaimer
This project is for educational purposes only. No real user data or unauthorized systems were targeted. Always get consent before testing any network or system.

