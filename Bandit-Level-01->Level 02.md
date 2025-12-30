## 🏴‍☠️ Bandit Level 01 → Level 02

---

### 🎯 Objective
- Log in to the Bandit server as `bandit1`
- Locate the file with a special name
- Read the file to obtain the password for the next level

---

### 🧭 Quick Action Summary
- Login as `bandit1`
- List files in the home directory
- Identify the file named `-`
- Read the file using a safe path reference
- Extract the password

---

### 🔑 Credentials Provided
- **Username:** `bandit1`
- **Password:** *(from previous level)*

---

### 🔍 Method of Solve
The password for the next level is stored in a file named `-`.  
Since `-` is interpreted as standard input by many commands, it cannot be read directly using `cat -`.

To solve this, the file must be referenced using a **relative path** (`./-`) so the shell treats it as a filename.

---

### 🧪 Steps Followed

1. **List all files**
```bash
ls
```
---

### 🧩 Commands Used

| Command   | Purpose |
|----------|---------|
| `ls`     | Lists files in the current directory |
| `cat ./-` | Reads a file with a special character name |

---

### 📸 Screenshot Evidence


---<img width="576" height="105" alt="Screenshot 2025-12-30 233526" src="https://github.com/user-attachments/assets/afa97e19-f4ad-4d6b-b4b5-06761064da68" />


### 🔑 Next Level Password
```text
263JGJPfgU6LtdEvqfWU1XP5yac29mFx
```
---
## 🧠 Explanation

- The `ls` command reveals a file named `-`
- Using `cat -` fails because `-` represents **standard input**
- Prefixing the filename with `./` forces the shell to treat it as a file
- `cat ./-` successfully displays the password

---

## 🔐 Concept Learned

This level teaches how Linux handles **special characters in filenames** and how **relative paths** can be used to safely access such files.

---

## 🛡️ Security Insight

Using confusing or special-character filenames can hide sensitive data, but **security through obscurity is not reliable**.  
Proper permissions and encryption should always be used.

  
