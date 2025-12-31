## 🏴‍☠️ Bandit Level 09 → Level 10

---

### 🎯 Objective
- Log in as `bandit9`
- Analyze `data.txt`
- Extract the password hidden among readable strings

---

### 🧭 Quick Action Summary
- List files
- Extract readable strings from a binary file
- Filter lines containing `=`
- Identify the password

---

### 🧪 Commands Used
```bash
ls
strings data.txt | grep "="
```
---
### 📸 Screenshot Evidence

<img width="931" height="397" alt="Screenshot 2025-12-31 102159" src="https://github.com/user-attachments/assets/35731630-90bd-4357-aa9f-d8453fe39c1b" />

---
### 🔑 Next Level Password
```
FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey
```
---
### 🧠 Explanation
- `data.txt` contains a mix of binary and readable text  
- The `strings` command extracts human-readable strings from the file  
- `grep "="` filters lines that contain an equals sign  
- The password is clearly visible among the filtered output  

---

### 🔐 Concept Learned
This level demonstrates how to:
- Extract readable data from binary files  
- Combine commands using pipes (`|`)  
- Filter useful information using `grep`  

---

### 🛡️ Security Insight
Hiding secrets inside binary files is **not secure**.  
Attackers can easily extract readable content using simple tools like `strings`.

Secure systems must rely on:
- Strong file permissions  
- Encryption  
- Least-privilege access  

---

