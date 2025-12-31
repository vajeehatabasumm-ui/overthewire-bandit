## 🏴‍☠️ Bandit Level 16 → Level 17
---
### 🎯 Objective
- Log in as `bandit16`
- Connect to a local SSL-enabled port
- Retrieve the RSA private key
- Use the key to log in as `bandit17`

---
### 🧭 Quick Action Summary
- Use `ncat` with `--ssl` to connect to port `31790`
- Receive the RSA private key
- Save the key to a file (e.g., `key17`)
- Set proper permissions: `chmod 600 key17`
- SSH into `bandit17` using the key

---
### 🧪 Commands Used
```bash
ncat localhost 31790 --ssl
# Copy the RSA key output
chmod 600 key17
ssh -i key17 bandit17@bandit.labs.overthewire.org -p 2220
cat /etc/bandit_pass/bandit17
```
---
### 📸 Screenshot Evidence
<img width="556" height="797" alt="Screenshot 2025-12-31 111651" src="https://github.com/user-attachments/assets/9f54759e-0de8-451d-89ae-3109563200c3" />
<img width="551" height="54" alt="Screenshot 2025-12-31 112316" src="https://github.com/user-attachments/assets/e958d96e-5128-47cc-91a5-07a0283a9c59" />


### Next Level Password
```
EReVavePLFHtFLFsjn3hyzMLvSuSAcRD
```
---
### 🧠 Explanation  
- The Bandit server runs a service on port `31790` that returns a private key when accessed via SSL  
- `ncat` with `--ssl` securely connects and retrieves the key  
- The key is used to authenticate as `bandit17` via SSH  
- The password for the next level is stored in `/etc/bandit_pass/bandit17`  

---

### 🔐 Concept Learned  
This level demonstrates how to:  
- Use `ncat` for SSL connections  
- Handle RSA private keys securely  
- Use key-based authentication with SSH  
- Read protected files after privilege escalation  

---

### 🛡️ Security Insight  
Private keys must be:  
- Stored securely with strict permissions  
- Never exposed in plaintext  
- Used with proper access controls  

Misuse or leakage of private keys can lead to unauthorized access.
