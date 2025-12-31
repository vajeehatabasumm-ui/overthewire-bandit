## 🏴‍☠️ Bandit Level 24 → Level 25
---
### 🎯 Objective
- Log in as `bandit24`
- Execute the pincode checker script
- Brute-force the correct password and pincode combination

---
### 🧭 Quick Action Summary
- Create a brute-force script (`brute.sh`) in `/tmp`
- Make the script executable
- Run the script to test multiple combinations
- Capture the successful output

---
### 🧪 Commands Used
```bash
cd /tmp
nano brute.sh
chmod +x brute.sh
./brute.sh
```
---
### 📸 Screenshot Evidence

<img width="960" height="310" alt="Screenshot 2025-12-30 175651" src="https://github.com/user-attachments/assets/a1fcaa60-eced-4468-9b1d-00c383c081ab" />

<img width="957" height="353" alt="Screenshot 2025-12-30 175626" src="https://github.com/user-attachments/assets/2110869d-17c0-493d-841f-91033bffe04f" />

---
### 🔑 Next Level Password
```
iCi6t8tT4K5Ne1earniKiwbQNmB3YJP3q4
```
---
### 🧠 Explanation  
- The pincode checker script prompts for the current password and a secret pincode  
- Multiple incorrect attempts result in "Wrong!" messages  
- Once the correct combination is found, the script outputs "Correct!" and reveals the password for `bandit25`  
- This level simulates brute-force logic and input automation  

---

### 🔐 Concept Learned  
This level demonstrates how to:  
- Automate input testing using shell scripts  
- Understand brute-force logic and response handling  
- Capture and parse output from interactive scripts  

---

### 🛡️ Security Insight  
Brute-force attacks are noisy and detectable but still effective against weak authentication mechanisms.  

Best practices include:  
- Rate-limiting login attempts  
- Using multi-factor authentication  
- Monitoring for repeated failed logins



