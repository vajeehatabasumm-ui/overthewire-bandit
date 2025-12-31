## 🏴‍☠️ Bandit Level 11 → Level 12
---
### 🎯 Objective
- Log in as `bandit11`
- Analyze `data.txt`
- Decode the ROT13-encoded password

---
### 🧭 Quick Action Summary
- List files in the directory
- View contents of `data.txt`
- Decode ROT13 using `tr`
- Extract the password

---
### 🧪 Commands Used
```bash
ls
cat data.txt
cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'
```
---
### 📸 Screenshot Evidence

<img width="959" height="184" alt="Screenshot 2025-12-31 103306" src="https://github.com/user-attachments/assets/3a16c0c3-6409-4d63-90ae-4db35681e136" />

---
### 🔑 Next Level Password
```
7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4
```
### 🧠 Explanation  
- data.txt contains a ROT13-encoded string  
- ROT13 is a simple substitution cipher that shifts letters by 13 positions  
- The tr command translates characters using ROT13  
- The decoded string reveals the password  

---

### 🔐 Concept Learned  
This level demonstrates how to:  
- Use cat to read file contents  
- Apply character translation with tr  
- Decode ROT13-encoded messages  

---

### 🛡️ Security Insight  
ROT13 is not encryption — it's a basic obfuscation method. Anyone with access to the file can decode it easily.  

Secure systems should use:  
- Strong encryption algorithms  
- Proper access controls  
---
