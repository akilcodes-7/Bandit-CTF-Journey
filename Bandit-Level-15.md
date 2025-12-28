## Bandit Level 15 → Level 16


### 🎯 Objective  

- Log in as `bandit15`  
- Connect to the SSL-enabled local service  
- Send the current password securely  
- Retrieve the password for the next level  


---

### 🧭 Quick Action Summary  

- Login as `bandit15`  
- Establish an SSL connection on port `30001`  
- Provide the current password  
- Receive the new password  


---

### 🔑 Credentials Provided  

- **Username:** bandit15  
- **Password:** 8xCjnmgoKbGLhFAZlGE5Tmu4M2tKJQo  


---

### 🔍 Method of Solve  

A secure service is running on port `30001` on the local machine.  
The password must be sent over an SSL-encrypted connection to retrieve the next level password.

Steps followed:  
- Connect to the service using SSL  
- Enter the current password  
- Receive the returned password  


---

### 🧪 Commands Used  

- `ncat --ssl localhost 30001`  


---

### 🧩 Command Purpose  

| Command | Purpose |
|--------|--------|
| `ncat --ssl localhost 30001` | Connects securely to the SSL-enabled service |


---

### 📸 Screenshot Evidence  

![Bandit Level 15 Screenshot](screenshots/level15.png)


---

### 🔑 Next Level Password  

```
kSkvUpMQ71BYvCM4GBPvCvT1BfWrQDx
```


---

### 🧠 Explanation  

- The `ncat --ssl` command creates an encrypted connection to the local service  
- The password is transmitted securely over SSL  
- The service validates the password and returns the next level’s credentials  


---

### 🔐 Concept Learned  

This level introduces secure communication using SSL.  
It highlights how encryption protects sensitive data during network transmission.


---

### 🛡️ Security Insight  

Unencrypted services can expose credentials in transit.  
Using SSL ensures data confidentiality and prevents interception.
