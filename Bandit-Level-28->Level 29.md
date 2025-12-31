## 🏴‍☠️ Bandit Level 28 → Level 29
---

### 🎯 Objective
- Log in as **bandit28**
- Clone the provided Git repository
- Inspect commit history
- Recover leaked credentials from previous commits

---

### 🧭 Quick Action Summary
- Create a working directory
- Clone the remote Git repository via SSH
- Read the README file
- Inspect Git commit history
- Use `git log -p` to view removed (leaked) data
- Extract the password from an earlier commit

---

### 🧪 Commands Used
```bash
cd /tmp
mkdir bob
cd bob

git clone ssh://bandit28-git@bandit.labs.overthewire.org:2220/home/bandit28-git/repo
cd repo

ls
cat README.md

git log
git log -p
```
### 🔍 Key Findings
- The latest **README.md** masks the password using `xxxxxxxxxx`
- **Older Git commits** still contain the original password
- Using **`git log -p`** reveals deleted content highlighted in **red**
- The password was exposed in an **earlier commit** before being removed

---

### 📸 Screenshot Evidence
- Repository successfully cloned from the Bandit Git server
- `README.md` file inspected
- Git commit history reviewed using `git log`
- Password clearly visible in the **diff of an earlier commit**

<img width="957" height="936" alt="Screenshot 2025-12-30 185818" src="https://github.com/user-attachments/assets/c73799f5-67ff-4404-b257-c9df7f693cfa" />

<img width="890" height="751" alt="Screenshot 2025-12-30 185837" src="https://github.com/user-attachments/assets/d3c3c0d9-28ab-4284-8363-e2b06ed9530e" />

---
🔑 Next Level Password
```
4pT1t5DENaYuqnqvadYs1oE4QLCdjmJ7
```
---
### 🧠 Explanation
Git tracks **all changes forever**, even data that has been deleted.

Using:
- **`git log`** → lists commit history
- **`git log -p`** → shows exact file changes, including removed secrets

The password was:
- Added in an early commit
- Later replaced with `xxxxxxxxxx`
- Still recoverable from Git history

---

### 🔐 Concept Learned
This level demonstrates that:
- Git **does not erase secrets**
- Deleted data remains accessible
- Sensitive information should **never be committed**

---

### 🛡️ Security Insight
Storing credentials in Git repositories is dangerous.

Even if removed:
- Attackers can recover secrets from commit history

✅ **Best practices:**
- Never commit passwords
- Use `.gitignore` for sensitive files
- Rotate credentials immediately if leaked
- Use secret managers

