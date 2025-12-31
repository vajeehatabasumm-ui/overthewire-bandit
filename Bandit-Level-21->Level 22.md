## 🏴‍☠️ Bandit Level 21 → Level 22
---
### 🎯 Objective
- Log in as `bandit21`
- Investigate the cron job for `bandit22`
- Retrieve the password written to a temporary file

---
### 🧭 Quick Action Summary
- Navigate to `/etc/cron.d/` and inspect `cronjob_bandit22`
- Read the script `/usr/bin/cronjob_bandit22.sh`
- Locate the output file in `/tmp/`
- Read the password from the file

---
### 🧪 Commands Used
```bash
cd /etc/cron.d/
ls -al
cat cronjob_bandit22
cat /usr/bin/cronjob_bandit22.sh
cat /tmp/t706LdS9SORqhQhaMzc6ShpAoZKf7Fgv
```
---
### 📸 Screenshot Evidence

<img width="575" height="409" alt="Screenshot 2025-12-31 123801" src="https://github.com/user-attachments/assets/e9bd60f8-5216-43cd-87a5-0ce9e46f49da" />

---
### 🔑 Next Level Password
```
tRae0UfB9v0UzBcdn9cY0gQnds9GF58Q
```
---
### 🧠 Explanation  
- The cron job for `bandit22` runs every minute and writes its password to a file in `/tmp/`  
- The script `cronjob_bandit22.sh` uses `cat` to copy the password into that file  
- By inspecting the cron job and reading the output file, you can retrieve the password  

---

### 🔐 Concept Learned  
This level demonstrates how to:  
- Analyze cron job configurations  
- Understand script execution and redirection  
- Locate and read temporary output files  

---

### 🛡️ Security Insight  
Cron jobs must be carefully managed to avoid leaking sensitive data.  

Best practices include:  
- Avoid writing secrets to world-readable locations  
- Use secure file permissions  
- Monitor scheduled tasks for unintended exposure  

---




