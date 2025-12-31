## 🏴‍☠️ Bandit Level 19 → Level 20
---
### 🎯 Objective
- Log in as `bandit19`
- Use the `bandit20-do` executable to run a command as `bandit20`
- Retrieve the password for the next level

---
### 🧭 Quick Action Summary
- List files in the home directory
- Run `bandit20-do` with a command to read the password file
- Capture the output

---
### 🧪 Commands Used
```bash
ls
./bandit20-do cat /etc/bandit_pass/bandit20
```
---
### 📸 Screenshot Evidence

<img width="589" height="154" alt="Screenshot 2025-12-31 114804" src="https://github.com/user-attachments/assets/29e8823d-8a5d-4931-a151-55257952b1d6" />

---
### 🔑 Next Level Password
```
OQxahG8ZJ0VMN9Ghs7iOWSCfZyXOUbYO
```
---
### 🧠 Explanation  
- The `bandit20-do` executable allows you to run commands as the `bandit20` user  
- Running `cat /etc/bandit_pass/bandit20` through this tool reveals the password  
- This is a controlled example of privilege escalation  

---

### 🔐 Concept Learned  
This level demonstrates how to:  
- Use a wrapper tool to execute commands as another user  
- Access protected files using privilege escalation  
- Understand basic command substitution and file access control  

---

### 🛡️ Security Insight  
Privilege escalation tools must be tightly controlled.  

Best practices include:  
- Limiting allowed commands  
- Logging all usage  
- Ensuring proper user authentication 




