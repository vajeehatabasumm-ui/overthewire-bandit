## Bandit Level 13 → Level 14


### 🎯 Objective  

- Log in as `bandit13`  
- Use an SSH private key for authentication  
- Access the `bandit14` account  
- Retrieve the password for the next level  


---

### 🧭 Quick Action Summary  

- Login as `bandit13`  
- Copy the private SSH key  
- Set proper key permissions  
- Connect as `bandit14` using the key  
- Read the password file  


---

### 🔑 Credentials Provided  

- **Username:** bandit13  
- **Password:** FOSdwFscOcbaIiH0h8J2eUks2vdTDwAn  


---

### 🔍 Method of Solve  

Instead of a normal password, an SSH private key is provided.  
This key must be used to authenticate as `bandit14` in order to retrieve the next level’s password.

Steps followed:  
- Copy the private key from the server  
- Secure the key with proper permissions  
- Use the key to log in via SSH  
- Read the password file  


---

### 🧪 Commands Used  

- `scp -P 2220 bandit13@bandit.labs.overthewire.org:/home/bandit13/sshkey.private .`  
- `chmod 600 sshkey.private`  
- `ssh -i sshkey.private bandit14@bandit.labs.overthewire.org -p 2220`  
- `cd /etc/bandit_pass`  
- `cat bandit14`  


---

### 🧩 Command Purpose  

| Command | Purpose |
|--------|--------|
| `scp` | Securely copies the private key from the remote server |
| `chmod 600` | Restricts access to the private key |
| `ssh -i` | Logs in using the private key |
| `cat bandit14` | Displays the password for the next level |


---

### 📸 Screenshot Evidence  

**Step 1 – Private Key Extraction from Bandit Server**  

<img width="959" height="667" alt="Screenshot 2025-12-31 105722" src="https://github.com/user-attachments/assets/daa9bf5f-343d-40ca-bcc9-543deea891a4" />

**Step 2 – SSH Login Using Private Key**  

<img width="694" height="151" alt="Screenshot 2025-12-31 105741" src="https://github.com/user-attachments/assets/adc316a0-b70e-4507-a8a7-c6a4bcd04628" />


---

### 🔑 Next Level Password  

```
MU4WWeTyJk8R0of1qgmcBPaLh7LDCPvS
```


---

### 🧠 Explanation  

- The private key is copied from the Bandit server  
- File permissions are restricted so SSH will accept the key  
- The key is used to authenticate as `bandit14`  
- The password is read from the protected system directory  


---

### 🔐 Concept Learned  

This level introduces SSH key-based authentication.  
It demonstrates how private keys are used for secure, passwordless system access.


---

### 🛡️ Security Insight  

Private keys must be protected with strict permissions.  
If exposed, attackers could gain full access to systems without needing passwords.
