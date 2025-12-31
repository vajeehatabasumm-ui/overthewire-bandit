## Bandit Level 14 → Level 15


### 🎯 Objective  

- Log in as `bandit14`  
- Connect to the local service on port 30000  
- Send the current password  
- Retrieve the password for the next level  


---

### 🧭 Quick Action Summary  

- Login as `bandit14`  
- Connect to `localhost` on port `30000`  
- Provide the current password  
- Receive the new password  


---

### 🔑 Credentials Provided  

- **Username:** bandit14  
- **Password:** MU4WWeTyJk8R0of1qgmcBPaLh7LDCPvS  


---

### 🔍 Method of Solve  

A service is running on port `30000` on the local machine.  
By sending the current password to this service, it responds with the password for the next level.

Steps followed:  
- Connect to the service using Netcat  
- Enter the current password  
- Receive the returned password  


---

### 🧪 Commands Used  

- `nc localhost 30000`  


---

### 🧩 Command Purpose  

| Command | Purpose |
|--------|--------|
| `nc localhost 30000` | Connects to the local service running on port 30000 |


---

### 📸 Screenshot Evidence  

<img width="341" height="87" alt="Screenshot 2025-12-31 110101" src="https://github.com/user-attachments/assets/bd26493a-76e1-47e5-a656-912464798eb0" />

---

### 🔑 Next Level Password  

```
8xCjnmgoKbGLhFAZlGE5Tmu4M2tKJQo
```


---

### 🧠 Explanation  

- The `nc` command opens a TCP connection to the local service  
- After entering the current password, the service validates it  
- The service returns the password for the next level  


---

### 🔐 Concept Learned  

This level introduces basic network communication using Netcat.  
It shows how services can receive input and return sensitive information over a network connection.


---

### 🛡️ Security Insight  

Network services that return sensitive data should use strong authentication and encryption.  
Unprotected services can expose credentials to unauthorized users.
