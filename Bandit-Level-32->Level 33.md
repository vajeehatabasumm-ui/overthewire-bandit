## 🏴‍☠️ Bandit Level 32 → Level 33
---

### 🎯 Objective
- Log in as `bandit32`
- Escape the restricted uppercase shell
- Retrieve the password for `bandit33` from `/etc/bandit_pass/bandit33`

---

### 🧭 Quick Action Summary
- Attempt basic commands in restricted shell
- Switch to a real shell using `bash`
- Read the password file using `cat`

---

### 🧪 Commands Used
```bash
ls
$0
cat etc/bandit_pass/bandit33
bash
cat /etc/bandit_pass/bandit33
```
---
### 📸 Screenshot Evidence

<img width="956" height="251" alt="Screenshot 2025-12-30 203657" src="https://github.com/user-attachments/assets/95c58ae8-7c40-4418-a816-a81d131b3336" />

<img width="557" height="185" alt="Screenshot 2025-12-30 203713" src="https://github.com/user-attachments/assets/f21be11f-6741-49a4-8e06-dfa93062803f" />

---
### 🔑 Next Level Password
```
tQdtbs5D5i2vJwkO8mEyYEyTL8izoeJ0
```
---
### 🧠 Explanation
- The shell starts in a restricted mode where only uppercase commands are allowed.
- ls fails because it’s interpreted as LS, which is blocked.
- $0 reveals the shell type.
- Attempting cat with a relative path fails due to incorrect location.
- Switching to bash bypasses the restriction.
- The correct path /etc/bandit_pass/bandit33 reveals the password.
 
 ---
### 🔐 Concept Learned This level teaches how to:
- Recognize and escape restricted shells
- Use absolute paths for secure file access
- Understand shell behavior and command interpretation

---
### 🛡️ Security Insight Restricted shells can be bypassed if not properly enforced. To improve security:
- Use hardened shells with strict command whitelisting
- Monitor shell escapes and privilege escalations
- Apply least-privilege principles to shell environments




