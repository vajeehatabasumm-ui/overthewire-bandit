## 🏴‍☠️ Bandit Level 23 → Level 24
---
### 🎯 Objective
- Log in as `bandit23`
- Analyze the cron job for `bandit24`
- Exploit the script to extract the password

---
### 🧭 Quick Action Summary
- Inspect `/etc/cron.d/cronjob_bandit24`
- Read the script `/usr/bin/cronjob_bandit24.sh`
- Understand how it executes and deletes scripts from `/var/spool/bandit24/foo`
- Create a custom script in that directory to copy the password to `/tmp/`
- Wait for the cron job to execute your script

---
### 🧪 Commands Used
```bash
cat /etc/cron.d/cronjob_bandit24
cat /usr/bin/cronjob_bandit24.sh
mkdir /tmp/myscript
cd /tmp/myscript
nano getpass.sh
chmod +x getpass.sh
cat /tmp/bandit24_pass
```
----
### 📸 Screenshot Evidence
<img width="1443" height="706" alt="Screenshot 2025-12-30 174707" src="https://github.com/user-attachments/assets/b757b6ba-fa71-4575-9f7e-37e3ed9616ba" />

---
### 🔑 Next Level Password
```
gbKksEFF4yrVs6il55v6gwY5aVje5f0j
```
---
### 🧠 Explanation  
- The cron job for `bandit24` runs every minute and executes a script that deletes files in `/var/spool/bandit24/foo`  
- It runs any script owned by `bandit23` before deleting it  
- By placing a script there that copies the password to `/tmp/bandit24_pass`, you can retrieve it after execution  

---

### 🔐 Concept Learned  
This level demonstrates how to:  
- Analyze and exploit cron job behavior  
- Use script injection in writable directories  
- Understand file ownership and execution flow  

---

### 🛡️ Security Insight  
Writable cron directories can be dangerous if not properly secured.  

Best practices include:  
- Restricting write access to execution paths  
- Validating script ownership and content  
- Logging and monitoring cron job activity  



