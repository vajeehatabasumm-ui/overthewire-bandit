## 🏴‍☠️ Bandit Level 20 → Level 21
---
### 🎯 Objective
- Log in as `bandit20`
- Set up a listener to receive the password from a scheduled job

---
### 🧭 Quick Action Summary
- Identify the `suconnect` binary in the home directory
- Start a Netcat listener on port `2222`
- Wait for the cron job to connect and send the password

---
### 🧪 Commands Used
```bash
ls
nc -lvp 2222
```
---
### 📸 Screenshot Evidence
<img width="403" height="96" alt="Screenshot 2025-12-31 120330" src="https://github.com/user-attachments/assets/63ff6b31-5423-4eb8-8c9f-bee8eb8c9b5b" />

---
### 🔑 Next Level Password
```
EeoULMCra2q0dSkyj561DX7s1CpBuOBt
```
---
### 🧠 Explanation  
- A cron job runs every minute and connects to port `2222`  
- By starting a Netcat listener (`nc -lvp 2222`), you can capture the incoming connection  
- The job sends the password for `bandit21` directly to your listener  

---

### 🔐 Concept Learned  
This level demonstrates how to:  
- Use Netcat to listen on a port  
- Receive data from automated jobs  
- Understand basic cron job behavior and inter-process communication  

---

### 🛡️ Security Insight  
Automated jobs that transmit sensitive data must be secured.  

Best practices include:  
- Using encrypted channels  
- Authenticating endpoints  
- Avoiding hardcoded secrets in scheduled tasks  



