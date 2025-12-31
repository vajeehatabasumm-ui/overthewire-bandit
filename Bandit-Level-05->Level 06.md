## 🏴‍☠️ Bandit Level 05 → Level 06

---

### 🎯 Objective
- Log in to the Bandit server as `bandit5`
- Search through multiple directories
- Identify the file that matches specific conditions
- Extract the password for the next level

---

### 🧭 Quick Action Summary
- Login as `bandit5`
- Move into the `inhere` directory
- Search for a file that:
  - Is a regular file
  - Has a size of 1033 bytes
  - Is not executable
- Read the file to obtain the password

---

### 🔑 Credentials Provided
- **Username:** `bandit5`
- **Password:** *(from previous level)*

---

### 🔍 Method of Solve
Inside the `inhere` directory, there are many subdirectories.  
The correct file can be identified using **file attributes**, not by name.

The password file:
- Is a **regular file**
- Has an exact size of **1033 bytes**
- Is **not executable**

The `find` command allows filtering files based on these conditions.

---

### 🧪 Steps Followed

1.**List files in the home directory**
   ```bash
   ls
   ```
2.**Move into the inhere directory**
  ```
  cd inhere
  ```
3.**List all directories**
  ```
  ls -al
  ```
4.**Find the file matching the required conditions**
  ```
  find . -type f -size 1033c ! -executable
  ```
5.**Read the discovered file**
  ```
  cat ./maybehere07/.file2
  ```
### 🧩 Commands Used

| Command | Purpose |
|--------|---------|
| `ls` | Lists files and directories |
| `cd inhere` | Moves into the `inhere` directory |
| `ls -al` | Displays detailed directory listings |
| `find . -type f -size 1033c ! -executable` | Searches for files matching specific attributes |
| `cat ./maybehere07/.file2` | Reads the password file |

---

### 📸 Screenshot Evidence

---<img width="966" height="828" alt="Screenshot 2025-12-31 094951" src="https://github.com/user-attachments/assets/f4200fcc-ad56-47a0-bdb1-08f69daa0e22" />


### 🔑 Next Level Password
```text
HWAsnPhtq9AVKe0dmk45nxy20cvUa6EG
```
### 🧠 Explanation
- The `inhere` directory contains many subdirectories
- File names alone are not helpful
- The `find` command filters files based on size and permissions
- Only one file matches all required conditions
- Reading that file reveals the password

---

### 🔐 Concept Learned
This level teaches how to:
- Use **file attributes** to locate data
- Search deeply using the `find` command
- Identify files based on size and permissions

---

### 🛡️ Security Insight
Hiding sensitive data among many files is not secure.  
Attackers can easily filter files using attributes like size and permissions.  
Strong **access controls and encryption** are required to protect sensitive information.

---


