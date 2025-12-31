## 🏴‍☠️ Bandit Level 29 → Level 30
---

### 🎯 Objective
- Log in as **bandit29**
- Clone the Git repository
- Explore all branches
- Locate credentials hidden in a non-default branch

---

### 🧭 Quick Action Summary
- Clone the repository
- Inspect `README.md` on the master branch
- List all available branches
- Switch to the `dev` branch
- Review commit history using `git log -p`
- Extract the password from an earlier commit

---

### 🧪 Commands Used
```bash
git clone ssh://bandit29-git@bandit.labs.overthewire.org:2220/home/bandit29-git/repo
cd repo

cat README.md

git branch
git branch -a

git checkout dev
git log -p
```
---
### 🔍 Key Findings
- The **master branch** hides the password using `<no passwords in production!>`
- Multiple remote branches exist, including **`origin/dev`**
- The **dev branch** contains additional development data
- Using **`git log -p`** reveals a password added in an earlier commit
- The password is visible in the commit diff before being masked

---

### 📸 Screenshot Evidence
- Repository successfully cloned
- `README.md` inspected on the master branch
- Remote branches listed using `git branch -a`
- Switched to the `dev` branch
- Password visible in commit diff using `git log -p`

<img width="950" height="921" alt="Screenshot 2025-12-30 191101" src="https://github.com/user-attachments/assets/bf1e43bf-cc16-4de1-9efe-0a773b4d89ec" />

<img width="959" height="900" alt="Screenshot 2025-12-30 191122" src="https://github.com/user-attachments/assets/cb97bf91-33a2-47cf-ad70-185273fb0f05" />

---
### 🔑 Next Level Password
```
qp30ex3VLz5MDG1n91YowTv4Q8I7CDZL
```
---
### 🧠 Explanation
Git repositories may contain **multiple branches**, not just `master`.

Using:
- **`git branch -a`** → lists all local and remote branches
- **`git checkout dev`** → switches to the development branch
- **`git log -p`** → shows exact changes, including added secrets

The password was:
- Added in the **`dev` branch**
- Hidden on the **master branch**
- Still recoverable through commit history

---

### 🔐 Concept Learned
This level demonstrates that:
- Secrets may exist in **non-default branches**
- Git preserves all historical data
- Reviewing only `master` is not enough

---

### 🛡️ Security Insight
Sensitive data in development branches is a common mistake.

Even if hidden in production:
- Attackers can inspect other branches
- Commit history may expose secrets

✅ **Best practices:**
- Scan all branches before deployment
- Never store credentials in Git
- Use environment variables or secret managers
- Remove secrets and rotate credentials immediately
