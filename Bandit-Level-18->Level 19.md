## 🏴‍☠️ Bandit Level 18 → Level 19
---
### 🎯 Objective
- Log in as `bandit18`
- Retrieve the password stored in the `readme` file

---
### 🧭 Quick Action Summary
- Use SSH to log in to the Bandit server
- Read the `readme` file directly using a remote `cat` command

---
### 🧪 Command Used
```bash
ssh bandit18@bandit.labs.overthewire.org -p 2220 cat readme
```
---
### 📸 Screenshot Evidence

<img width="557" height="253" alt="Screenshot 2025-12-31 114153" src="https://github.com/user-attachments/assets/6a82d353-a471-42e3-b37c-b257c95d786a" />

---
###  🔑 Next Level Password
```
cGWpMaKXvvDUNGpAVJBWvYUGHYn9zL3j8
```
---
### 🧠 Explanation  
- The password for `bandit19` is stored in a file named `readme`  
- Instead of logging in and navigating manually, the password can be retrieved directly using SSH with a remote command (`cat readme`)  
- This technique saves time and demonstrates command chaining with SSH  

---

### 🔐 Concept Learned  
This level demonstrates how to:  
- Use SSH to execute remote commands  
- Retrieve file contents without interactive login  
- Chain commands for efficient access  

---

### 🛡️ Security Insight  
Remote command execution via SSH is powerful but must be used securely.  

Best practices include:  
- Using SSH keys instead of passwords  
- Restricting command execution with `authorized_keys` options  
- Monitoring SSH access logs  

---
