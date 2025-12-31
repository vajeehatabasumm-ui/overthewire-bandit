## 🏴‍☠️ Bandit Level 10 → Level 11

---

### 🎯 Objective
- Log in as `bandit10`
- Analyze `data.txt`
- Decode the Base64‑encoded content to extract the password

---

### 🧭 Quick Action Summary
- List files in the home directory
- Identify encoded data
- Decode Base64 content
- Reveal the password

---

### 🧪 Commands Used
```bash
ls
base64 -d data.txt
```
---
### 📸 Screenshot Evidence
<img width="707" height="132" alt="Screenshot 2025-12-31 102546" src="https://github.com/user-attachments/assets/fb39b1c3-610e-486f-a08d-053122e831e4" />

---
### 🔑 Next Level Password
```
dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr
```
---
### 🧠 Explanation
- `data.txt` contains **Base64‑encoded text**
- The `base64 -d` command decodes the encoded data
- Once decoded, the **password is displayed in plain text**

---

### 🔐 Concept Learned
This level demonstrates how to:
- Identify encoded data
- Decode Base64 strings using Linux command‑line tools
- Understand basic data‑encoding techniques

---

### 🛡️ Security Insight
- **Encoding is not encryption.** Base64 only obscures data and can be easily reversed.
- Secure systems should rely on:
  - Strong encryption
  - Proper access controls
  - Least‑privilege permissions
