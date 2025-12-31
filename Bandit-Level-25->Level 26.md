## 🏴‍☠️ Bandit Level 25 → Level 26

---

### 🎯 Objective
- Log in as `bandit25`
- Locate the SSH private key for `bandit26`
- Transfer the key to the local machine
- Use the key to log in as `bandit26`

---

### 🧭 Quick Action Summary
- Identify the SSH key file
- Copy the key using `scp`
- Verify the key type
- Use the key for SSH authentication

---

### 🧪 Commands Used
```bash
# On bandit25
ls
file bandit26.sshkey
exit

# On local machine (Kali)
scp -P 2220 bandit25@bandit.labs.overthewire.org:/home/bandit25/bandit26.sshkey .
file bandit26.sshkey
ssh -i bandit26.sshkey bandit26@bandit.labs.overthewire.org -p 2220
```
---
### 📸 Screenshot Evidence
<img width="948" height="793" alt="Screenshot 2025-12-31 132533" src="https://github.com/user-attachments/assets/49340303-4c04-4ffa-8a5b-6d8ff4aecbee" />

<img width="478" height="130" alt="Screenshot 2025-12-31 132548" src="https://github.com/user-attachments/assets/a24ea8d5-5f0c-47db-9f84-6b8b742b74fd" />

---
### 🔑 Next Level Password
```
s0773xxkk0MXfdQfPRvR9L3jJBUOgCZ
```
---
### 🧠 Explanation
- The home directory of `bandit25` contains a file named `bandit26.sshkey`
- The `file` command confirms it is a **PEM RSA private key**
- The key is copied to the local system using `scp` over port `2220`
- SSH authentication is performed using the `-i` option to specify the private key
- Once logged in as `bandit26`, the password file `/etc/bandit_pass/bandit26` can be read

---

### 🔐 Concept Learned
This level demonstrates how to:
- Identify SSH private keys
- Transfer files securely using `scp`
- Authenticate using SSH key-based login
- Troubleshoot common SSH command mistakes

---

### 🛡️ Security Insight
- **Private SSH keys must be protected**
- Exposed keys allow full account access
- Secure systems should:
  - Restrict key file permissions
  - Avoid storing private keys in readable locations
  - Use passphrases for SSH keys
  - Rotate compromised credentials
