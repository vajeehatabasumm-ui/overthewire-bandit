## 🏴‍☠️ Bandit Level 26 → Level 27

---

### 🎯 Objective
- Log in as `bandit26` using an SSH key
- Use the provided executable to run commands as `bandit27`
- Read the password file for the next level

---

### 🧭 Quick Action Summary
- Connect using SSH with a private key
- Identify special executable files
- Use the executable to run commands as another user
- Read the password file

---

### 🧪 Commands Used
```bash
ssh -i bandit26.sshkey bandit26@bandit.labs.overthewire.org -p 2220
ls
./bandit27-do cat /etc/bandit_pass/bandit27
```
---
### 📸 Screenshot Evidence

<img width="435" height="89" alt="Screenshot 2025-12-31 131412" src="https://github.com/user-attachments/assets/cfb58539-b8ad-454c-957b-d8e16cbe9357" />

<img width="451" height="214" alt="Screenshot 2025-12-31 131451" src="https://github.com/user-attachments/assets/b00bad70-2251-4e6a-a375-dcf4992186ad" />

<img width="577" height="220" alt="Screenshot 2025-12-31 131514" src="https://github.com/user-attachments/assets/1de0d73c-6e62-4be2-9e02-e18125a498b7" />

---
### 🔑 Next Level Password
```
upsNCc7vzaRDx6oZC6GiR6ERwe1MowGB
```
---
### 🧠 Explanation
- Login is performed using an **SSH private key** instead of a password
- The file `bandit27-do` is a **setuid executable**
- This executable allows running commands **as user `bandit27`**
- Using it to read `/etc/bandit_pass/bandit27` reveals the password

---

### 🔐 Concept Learned
This level demonstrates how to:
- Authenticate using SSH keys
- Identify and use privileged executables
- Execute commands as another user
- Understand Linux privilege escalation mechanisms

---

### 🛡️ Security Insight
- **Setuid binaries are powerful and dangerous if misconfigured**
- Attackers can exploit them to escalate privileges
- Secure systems must:
  - Minimize setuid usage
  - Restrict executable permissions
  - Follow the principle of least privilege
