## 🏴‍☠️ Bandit Level 03 → Level 04

---

### 🎯 Objective
- Log in to the Bandit server as `bandit3`
- Locate a hidden file inside a directory
- Read the hidden file to obtain the password for the next level

---

### 🧭 Quick Action Summary
- Login as `bandit3`
- List files in the home directory
- Enter the `inhere` directory
- List **all files including hidden files**
- Read the hidden file
- Extract the password

---

### 🔑 Credentials Provided
- **Username:** `bandit3`
- **Password:** *(from previous level)*

---

### 🔍 Method of Solve
The password for the next level is stored in a **hidden file** inside the `inhere` directory.  
Hidden files in Linux start with a dot (`.`) and are not visible with the normal `ls` command.

Using `ls -al` allows us to list **all files**, including hidden ones, so the password file can be identified and read.

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
   **Read the hidden file**
   ```bash
   cat ...Hiding-From-You
  ```
---
### 🧩 Commands Used

| Command | Purpose |
|--------|---------|
| `ls` | Lists files in the directory |
| `cd inhere` | Moves into the `inhere` directory |
| `ls -al` | Shows all files including hidden files |
| `cat ...Hiding-From-You` | Reads the hidden password file |

---

### 📸 Screenshot Evidence


---<img width="913" height="297" alt="Screenshot 2025-12-30 235755" src="https://github.com/user-attachments/assets/d792a4d7-f0bf-4c8d-bf14-e3e9e08cb7fb" />


### 🔑 Next Level Password
```text
2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ
```
---
### 🧠 Explanation
- The `ls` command shows the `inhere` directory
- Hidden files are not visible using the normal `ls` command
- The `ls -al` command reveals a hidden file named `...Hiding-From-You`
- Using `cat` on the hidden file displays the password

---

### 🔐 Concept Learned
This level demonstrates how Linux uses **hidden files** (files starting with a dot) and how they can store sensitive information that is not immediately visible.

---

### 🛡️ Security Insight
Hidden files do **not** provide real security.  
Anyone with basic Linux knowledge can discover them easily.  
Sensitive data should always be protected using proper permissions and encryption.
