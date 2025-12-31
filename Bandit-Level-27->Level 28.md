## 🏴‍☠️ Bandit Level 27 → Level 28

---

### 🎯 Objective
- Log in as `bandit27`
- Clone the remote Git repository
- Locate the password inside the repository

---

### 🧭 Quick Action Summary
- Move to a writable directory
- Clone the Git repository using SSH
- Explore repository contents
- Read the README file to obtain the password

---

### 🧪 Commands Used
```bash
cd /tmp
git clone ssh://bandit27-git@bandit.labs.overthewire.org:2220/home/bandit27-git/repo
cd repo
cat README
```
---
### 📸 Screenshot Evidence

<img width="955" height="573" alt="Screenshot 2025-12-30 185312" src="https://github.com/user-attachments/assets/05a01053-a2ea-4355-8a77-a471a95cfc74" />

---
### 🔑 Next Level Password
```
Yz9IpLoSBcCeuG7m9uQFt8ZNpS4HZRcn
```
---
### 🧠 Explanation
- The level provides access to a **remote Git repository**
- The repository must be cloned to a writable directory such as `/tmp`
- Git uses **SSH authentication** on port `2220`
- After cloning, the repository contents can be explored locally
- The password is stored directly inside the `README` file

---

### 🔐 Concept Learned
This level demonstrates how to:
- Clone Git repositories over SSH
- Work with remote repositories
- Navigate repository files
- Extract sensitive information from version control systems

---

### 🛡️ Security Insight
- **Sensitive data should never be stored in repositories**
- Public or exposed repositories can easily leak credentials
- Secure practices include:
  - Using secrets managers
  - Removing credentials from version history
  - Restricting repository access
  - Auditing commits regularly
