## 🏴‍☠️ Bandit Level 31 → Level 32
---

### 🎯 Objective
- Log in as **bandit31**
- Clone the Git repository
- Add the required file
- Commit and push changes to the remote repository
- Receive the password for the next level

---

### 🧭 Quick Action Summary
- Navigate to the repository
- Verify required files
- Force add the required file
- Configure Git user details
- Commit changes
- Push to the remote repository

---

### 🧪 Commands Used
```bash
ls

git add key.txt -f
git config user.email "bandit31@localhost"

git commit -m "Add key.txt file"
git push origin master
```
---
### 🔍 Key Findings
- The repository already contains a `key.txt` file
- The file is normally ignored and must be **force-added**
- Git requires user identity configuration before committing
- Pushing the commit triggers server-side validation
- The server reveals the password after successful validation

---

### 📸 Screenshot Evidence
- Repository contents verified
- `key.txt` force-added using `-f`
- Commit created successfully
- Changes pushed to the remote repository
- Password returned by the server after validation

<img width="956" height="265" alt="Screenshot 2025-12-30 201338" src="https://github.com/user-attachments/assets/cc294608-1b33-4661-a825-7e2ef1c4e49b" />

<img width="861" height="609" alt="Screenshot 2025-12-31 135421" src="https://github.com/user-attachments/assets/8ed0ea73-a1f4-4068-ae2c-3107fea26e1a" />

---
### 🔑 Next Level Password
```
309RfhqyALVBEZpVb6LYStshZoqoSx5K
```
---
### 🧠 Explanation
Some repositories restrict files using ignore rules.

Using:
- **`git add -f`** → forces addition of ignored files
- **`git commit`** → records changes locally
- **`git push`** → sends changes to the remote server

The server validates:
- File presence
- Correct commit structure
- Successful push

Once validated, the password is revealed.

---

### 🔐 Concept Learned
This level demonstrates that:
- Ignored files can still be committed if forced
- Git requires proper user configuration
- Server-side hooks can validate repository state

---

### 🛡️ Security Insight
Server-side Git hooks are useful for enforcing rules.

However:
- Forced commits can bypass ignore protections
- Validation must be strict and well-designed

✅ **Best practices:**
- Use server-side hooks carefully
- Avoid relying solely on `.gitignore`
- Validate file contents, not just presence
- Rotate secrets immediately after exposure

