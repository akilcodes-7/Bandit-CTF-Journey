## Bandit Level 19 → Level 20


### 🎯 Objective  

- Log in as `bandit19`  
- Identify the set-UID executable  
- Use it to run commands as `bandit20`  
- Retrieve the password for the next level  


---

### 🧭 Quick Action Summary  

- Login as `bandit19`  
- Locate the `bandit20-do` binary  
- Use it to execute a privileged command  
- Read the password file  


---

### 🔑 Credentials Provided  

- **Username:** bandit19  
- **Password:** cGWpMaKXWDUNpPAJwbYUGHv9szJ3j8  


---

### 🔍 Method of Solve  

A special executable file named `bandit20-do` is owned by `bandit20` and has the set-UID bit enabled.  
When this file is executed, it runs commands with `bandit20` privileges.

Steps followed:  
- List files and check permissions  
- Identify the set-UID binary  
- Use it to run a command as `bandit20`  
- Read the password file  


---

### 🧪 Commands Used  

- `ls -la`  
- `./bandit20-do cat /etc/bandit_pass/bandit20`  


---

### 🧩 Command Purpose  

| Command | Purpose |
|--------|--------|
| `ls -la` | Displays file permissions and ownership |
| `./bandit20-do cat ...` | Executes a command as `bandit20` using the set-UID binary |


---

### 📸 Screenshot Evidence  

![Bandit Level 19 Screenshot](screenshots/level19.png)


---

### 🔑 Next Level Password  

```
oqXahG8ZjOVMN9Ghs710WsCfZyXOUbY0
```


---

### 🧠 Explanation  

- The set-UID bit allows the binary to run with the owner’s privileges  
- `bandit20-do` is owned by `bandit20`  
- Using it allows access to `/etc/bandit_pass/bandit20`  
- The file contains the password for the next level  


---

### 🔐 Concept Learned  

This level demonstrates the use of set-UID binaries.  
It shows how controlled privilege escalation works in Linux systems.


---

### 🛡️ Security Insight  

Misconfigured set-UID binaries can lead to serious security risks.  
They must be carefully controlled to prevent unauthorized privilege escalation.
