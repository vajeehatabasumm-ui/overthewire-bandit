## Bandit Level 17 → Level 18


### 🎯 Objective  

- Log in as `bandit17`  
- Locate the password files  
- Compare the old and new versions  
- Retrieve the password for the next level  


---

### 🧭 Quick Action Summary  

- Login as `bandit17`  
- Identify `passwords.new` and `passwords.old`  
- Compare both files  
- Extract the new password  


---

### 🔑 Credentials Provided  

- **Username:** bandit17  
- **Password:** password from previous bandit16  


---

### 🔍 Method of Solve  

Two files contain different versions of password data.  
By comparing them, the newly added password can be identified.

Steps followed:  
- List all files  
- Compare the two password files  
- Identify the new entry  


---

### 🧪 Commands Used  

- `ls`  
- `diff passwords.new passwords.old`  


---

### 🧩 Command Purpose  

| Command | Purpose |
|--------|--------|
| `ls` | Lists files in the current directory |
| `diff passwords.new passwords.old` | Shows differences between two files |


---

### 📸 Screenshot Evidence  


<img width="463" height="123" alt="Screenshot 2025-12-31 113820" src="https://github.com/user-attachments/assets/7f7be54e-cbd5-4334-b0c2-065c89f066a6" />

---

### 🔑 Next Level Password  

```
x2gLTTjFwMOHQ80WNbMN36ZQKxFrQGIO
```


---

### 🧠 Explanation  

- The `diff` command highlights lines that differ between the two files  
- Lines present only in `passwords.new` represent newly added entries  
- The new entry is the password for the next level  


---

### 🔐 Concept Learned  

This level demonstrates how file comparison can be used to track changes.  
It shows how identifying differences is useful in system auditing and security analysis.


---

### 🛡️ Security Insight  

Password changes should be carefully tracked and protected.  
Unauthorized access to versioned files can expose sensitive credentials.
