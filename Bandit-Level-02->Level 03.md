## 🏴‍☠️ Bandit Level 02 → Level 03

---

### 🎯 Objective
- Log in to the Bandit server as `bandit2`
- Locate the file that contains spaces in its name
- Read the file to obtain the password for the next level

---

### 🧭 Quick Action Summary
- Login as `bandit2`
- List files in the home directory
- Identify the file with spaces in its name
- Read the file using escaped spaces
- Extract the password

---

### 🔑 Credentials Provided
- **Username:** `bandit2`
- **Password:** *(from previous level)*

---

### 🔍 Method of Solve
The password for the next level is stored in a file whose name contains **spaces**.  
Linux treats spaces as separators, so the filename must be handled carefully using **escape characters (`\`)** or quotes to correctly read the file.

---

### 🧪 Steps Followed


   ```bash
   ls
   cat --spaces\ in\ this\ filename--
   ```
   ---
   ### 🧩 Commands Used

| Command | Purpose |
|--------|---------|
| `ls` | Lists files in the current directory |
| `cat --spaces\ in\ this\ filename--` | Reads a file that contains spaces in its name |

---

### 📸 Screenshot Evidence

<img width="724" height="99" alt="Screenshot 2025-12-30 234939" src="https://github.com/user-attachments/assets/f2eaa353-c57f-4bb0-a07d-235f42e30284" />

---
### 🔑 Next Level Password
```text
MNk8KNH3Usiio41PRUEoDFPqfxLPLSmx
```
---
### 🧠 Explanation
- The `ls` command shows a file named `--spaces in this filename--`
- Filenames with spaces cannot be read directly without special handling
- Using `\` escapes each space so the shell reads the full filename correctly
- The `cat` command then displays the password successfully

---

### 🔐 Concept Learned
This level demonstrates how Linux handles **filenames with spaces** and introduces the concept of **escaping characters** to safely access such files.

---

### 🛡️ Security Insight
Using spaces or unusual filenames may slow attackers, but it does **not provide real security**.  
Strong file permissions and proper encryption are essential for protecting sensitive data.


