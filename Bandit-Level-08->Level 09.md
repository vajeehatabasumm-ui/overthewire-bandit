## 🏴‍☠️ Bandit Level 08 → Level 09

---

### 🎯 Objective
- Find the password stored in a file where **only one line occurs once**
- All other lines occur multiple times

---

### 🧭 Quick Action Summary
- List files
- Sort file contents
- Count unique lines
- Identify the line that appears only once

---

### 🧪 Commands Used

| Command | Purpose |
|--------|---------|
| `ls -al` | Lists files with permissions and details |
| `sort data.txt` | Sorts the file alphabetically |
| `uniq -c` | Counts occurrences of each line |
| `sort \| uniq -c` | Finds unique line counts |

---

### 🧪 Steps Followed

```bash
ls -al
sort data.txt | uniq -c
```
---
### 📸 Screenshot Evidence

---<img width="964" height="409" alt="Screenshot 2025-12-31 101558" src="https://github.com/user-attachments/assets/40dd8ec3-e2b8-49f0-81f1-1212a66404c1" />

---
### 🔑 Next Level Password
```
4CKMh1JI91bUIZZPXDQGanal4xvAg0JM
```
---
### 🧠 Explanation
- `data.txt` contains many repeated lines  
- The file must be **sorted first** for `uniq` to work correctly  
- `uniq -c` counts how many times each line appears  
- The password is the line that appears **only once**

---

### 🔐 Concept Learned
This level teaches how to:
- Process large text files
- Use command pipelines (`|`)
- Detect unique data using `sort` and `uniq`
- Analyze frequency-based patterns

---

### 🛡️ Security Insight
Repeating sensitive data multiple times does not provide security.  
Attackers can easily detect anomalies using basic text-processing tools.

Always protect sensitive data with:
- Proper permissions
- Encryption
- Least-privilege access

---

