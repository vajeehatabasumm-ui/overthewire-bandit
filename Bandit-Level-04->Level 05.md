## 🏴‍☠️ Bandit Level 04 → Level 05

---

### 🎯 Objective
- Log in to the Bandit server as `bandit4`
- Locate the directory containing multiple files
- Identify the file that contains readable ASCII text
- Extract the password for the next level

---

### 🧭 Quick Action Summary
- Login as `bandit4`
- Enter the `inhere` directory
- List all files
- Identify file types
- Read the ASCII text file to obtain the password

---

### 🔑 Credentials Provided
- **Username:** `bandit4`
- **Password:** *(from previous level)*

---

### 🔍 Method of Solve
Inside the `inhere` directory, there are multiple files with similar names.  
Only **one file contains human-readable ASCII text**.  
By checking the file types using the `file` command, the correct file can be identified and read to obtain the password.

---

### 🧪 Steps Followed

**List files in the home directory** 
   ```bash
   ls
   ```
   **Move into the `inhere` directory**
   ```bash
   cd inhere
   ```
   **List all files including hidden files**
   ```bash
   ls -al
   ```
   **Identify file types**
   ```
   find . -type f | xargs file
   ```
   **Read the ASCII text file**
   ```bash
   cat ./-file07
  ```
---
## 🧩 Commands Used

| Command | Purpose |
|-------|--------|
| `ls` | Lists files in the directory |
| `cd inhere` | Moves into the `inhere` directory |
| `ls -al` | Shows detailed file listings |
| `file` | Identifies file types |
| `find . -type f | xargs file` | Checks file types for all files |
| `cat ./-file07` | Reads the readable ASCII file |
---
## 📸 Screenshot Evidence
<img width="838" height="696" alt="Screenshot 2025-12-31 001113" src="https://github.com/user-attachments/assets/027fe3d2-bb0f-44f1-b7cf-303e74f92554" />
---

## 🔑 Next Level Password
   ```
4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw
  ```
---
# Inhere Directory Analysis

🧠 **Explanation**

  The `inhere` directory contains multiple files with similar names.  
- Most files contain binary or encrypted data.  
- The `file` command identifies one file as ASCII text.  
- Reading that file using `cat` reveals the password.
---

🔐 **Concept Learned**  
This level teaches how to:  
- Analyze file types in Linux  
- Avoid blindly opening unknown files  
- Use command-line tools to locate meaningful data
---

🛡️ **Security Insight**  
- Relying on file obscurity does not protect sensitive data.  
- Attackers can easily analyze file types to locate readable information.  
- Proper file permissions, encryption, and access controls are essential for real security.

