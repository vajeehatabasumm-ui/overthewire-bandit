## 🧩 Bandit Level 6 → Level 7

### 🧠 Explanation
- The home directory does not contain the password
- The password file exists **somewhere on the system**
- We are given specific file attributes:
  - Owned by user `bandit7`
  - Belongs to group `bandit6`
  - File size is exactly `33 bytes`
- The `find` command is used to search the entire filesystem
- Error messages are redirected to `/dev/null` to keep output clean
- Only one file matches all conditions
- Reading that file reveals the password

---

### 🧩 Commands Used

```bash
ls -al
cd /
find . -type f -user bandit7 -group bandit6 -size 33c 2>/dev/null
cat /var/lib/dpkg/info/bandit7.password
```
---
### 📸 Screenshot Evidence


---<img width="957" height="357" alt="Screenshot 2025-12-31 100032" src="https://github.com/user-attachments/assets/8c2e1721-6ee5-4611-8573-3e1ed428aa38" />

---
### 🔑 Next Level Password

```
morbNTDkSW6jILuC0ymOdMaLnOLFVAaj
```
---
### 🔐 Concepts Learned
This level teaches how to:

- Search the **entire filesystem** using `find`
- Filter files by **user ownership**
- Filter files by **group ownership**
- Identify files using **exact file size**
- Suppress permission errors using `2>/dev/null`
---
### 🛡️ Security Insight
Relying on **file obscurity** is not secure.  
Even if files are hidden deep within the filesystem, attackers can locate them using metadata such as:

- File owner
- Group ownership
- File size

Proper security requires:

- **Strong access permissions**
- **Principle of least privilege**
- **Encryption for sensitive data**
