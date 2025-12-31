## 🏴‍☠️ Bandit Level 07 → Level 08

---

### 🎯 Objective
Find the password for the next level hidden inside a large text file.

---

### 🧪 Steps Followed

1. List files in the home directory  
2. Identify the large file `data.txt`  
3. Extract human-readable strings  
4. Search for the keyword **millionth**

---

### 🧪 Commands Used

```bash
ls -al
strings data.txt | grep "millionth"
```
---
### 📸 Screenshot Evidence

-<img width="958" height="379" alt="Screenshot 2025-12-31 100914" src="https://github.com/user-attachments/assets/1a91edda-1ab2-4e30-84e2-5ade41c31936" />
---
---
### 🔑 Next Level Password
```
dfwvzFQi4mU0wfNbF0e9RoWskMLg7eEc
```
---
### 🧠 Explanation
- `data.txt` contains a large amount of binary and text data  
- The `strings` command extracts readable text from the file  
- `grep "millionth"` filters the exact line containing the password  
- The password appears next to the keyword **millionth**

---

### 🔐 Concept Learned
This level demonstrates how to:
- Extract readable content from binary files
- Combine commands using pipes (`|`)
- Efficiently search large files

---

### 🛡️ Security Insight
Security through obscurity is ineffective.  
Even if data is hidden inside large or binary files, attackers can easily extract readable information.

**Always use:**
- Proper file permissions  
- Encryption  
- Least-privilege access
