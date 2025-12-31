## 🏴‍☠️ Bandit Level 30 → Level 31
---

### 🎯 Objective
- Log in as **bandit30**
- Clone the Git repository
- Inspect branches and tags
- Recover the password hidden in a Git tag

---

### 🧭 Quick Action Summary
- Clone the repository
- Inspect the README file
- Check available branches
- List Git tags
- Inspect the secret tag to extract the password

---

### 🧪 Commands Used
```bash
git clone ssh://bandit30-git@bandit.labs.overthewire.org:2220/home/bandit30-git/repo
cd repo

ls
cat README.md

git branch
git branch -a

git tag
git show-ref --tags
git show secret
```
---
### 🔍 Key Findings
- The `README.md` file appears empty and misleading
- No additional branches exist beyond `master`
- A Git **tag named `secret`** exists in the repository
- The tag points to hidden data not visible in the working tree
- Using **`git show secret`** reveals the password

---

### 📸 Screenshot Evidence
- Repository successfully cloned
- `README.md` inspected and found empty
- Branch list verified
- Git tag `secret` identified
- Password revealed using `git show secret`

<img width="907" height="344" alt="Screenshot 2025-12-30 191946" src="https://github.com/user-attachments/assets/830a4a5a-a579-41ed-983b-ec21a1d95b11" />

<img width="959" height="595" alt="Screenshot 2025-12-30 192010" src="https://github.com/user-attachments/assets/907da072-6f10-4515-a852-c3f468e95cf8" />

---

### 🔑 Next Level Password
```
fb5S2xb7bRyFmAvQYQGEgshbVyJghnDy
```
---
### 🧠 Explanation
Git tags can reference commits or objects that are not obvious during normal inspection.

Using:
- **`git tag`** → lists all tags
- **`git show-ref --tags`** → shows references to tagged objects
- **`git show <tag>`** → displays the content stored in the tag

The password was:
- Stored inside a Git tag
- Not visible in files or branches
- Recoverable by inspecting tag contents

---

### 🔐 Concept Learned
This level demonstrates that:
- Git tags may store sensitive data
- Hidden objects can exist outside branches
- Full repository inspection includes tags

---

### 🛡️ Security Insight
Sensitive data stored in Git tags is dangerous.

Even if files look empty:
- Tags can leak secrets
- Attackers can inspect all Git references

✅ **Best practices:**
- Audit tags before sharing repositories
- Never store credentials in tags
- Use secret management solutions
- Rotate credentials if exposure occurs
