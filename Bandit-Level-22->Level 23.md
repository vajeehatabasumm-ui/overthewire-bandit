## 🏴‍☠️ Bandit Level 22 → Level 23
---
### 🎯 Objective
- Log in as `bandit22`
- Investigate the cron job for `bandit23`
- Retrieve the password written to a hash-named file in `/tmp/`

---
### 🧭 Quick Action Summary
- Inspect `/etc/cron.d/cronjob_bandit23`
- Read the script `/usr/bin/cronjob_bandit23.sh`
- Generate the hash filename using `md5sum`
- Read the password from the generated file path

---
### 🧪 Commands Used
```bash
cd /etc/cron.d/
cat cronjob_bandit23
cat /usr/bin/cronjob_bandit23.sh
echo I am user bandit23 | md5sum | cut -d ' ' -f 1
cat /tmp/8ca319486bfbbc3663ea0fbe81326349
```
---
### 📸 Screenshot Evidence

<img width="769" height="620" alt="Screenshot 2025-12-31 124514" src="https://github.com/user-attachments/assets/758f6cc5-0d7e-45fc-b0de-d566f6c770cc" />

---
### 🔑 Next Level Password
```
02f1ii1JMvN551jX3CmStkVLqjKs4Ga
```
---
### 🧠 Explanation  
- The cron job for `bandit23` runs every minute and executes a script  
- The script generates a hash from the string `I am user bandit23` and uses it as a filename  
- It copies the password for `bandit23` into `/tmp/<hash>`  
- By replicating the hash logic, you can locate and read the password file  

---

### 🔐 Concept Learned  
This level demonstrates how to:  
- Analyze cron job scripts and logic  
- Use `md5sum` to generate predictable filenames  
- Understand dynamic file naming and privilege-based access  

---

### 🛡️ Security Insight  
Using predictable hashes for sensitive file names can expose secrets.  

Best practices include:  
- Using secure, random filenames  
- Limiting file access with proper permissions  
- Avoiding hardcoded logic that can be reverse-engineered  



