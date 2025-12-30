## 🏴‍☠️ Bandit Level 00 → Level 01

---

### 🎯 Objective
- Log in to the OverTheWire Bandit game using the provided credentials  
- Locate the `readme` file in the home directory  
- Retrieve the password for the next level  

---

### 🧭 Quick Action Summary
- Login as `bandit0`
- List files in the home directory
- Read the `readme` file
- Extract the password for Level 01

---

### 🔑 Credentials Provided
- **Username:** `bandit0`  
- **Password:** `bandit0`  

---

### 🔍 Method of Solve
The password for the next level is stored in a file named `readme` located in the home directory.  
By listing the available files and reading the contents of the `readme` file, the password can be obtained.

---

### 🧪 Steps Followed
- List all files
- Read the `readme` file

---

### 🧪 Commands Used

- `ls`
- `cat readme`

---
### 📸 Screenshot Evidence


<img width="961" height="274" alt="level00 png" src="https://github.com/user-attachments/assets/ca4c9b62-9c52-45af-a282-76161c40449e" />

---

### 🔑 Next Level Password
```text
ZjlJTmM6FvvyRnrB2rfNWOZOTa6ip5If
```
---

### 🧠 Explanation
- The `ls` command lists available files  
- The `readme` file contains the password  
- `cat readme` displays the password on the screen  

---

### 🔐 Concept Learned
This level introduces basic Linux file access.  
It shows how sensitive data can be stored in simple text files.

---

### 🛡️ Security Insight
Passwords stored in plain text files are highly insecure.  
Proper access controls and encryption should always be used.
