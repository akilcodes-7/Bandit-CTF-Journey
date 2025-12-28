## Bandit Level 18 → Level 19


### 🎯 Objective  

- Log in as `bandit18`  
- Execute a command during SSH login  
- Bypass the immediate logout  
- Retrieve the password for the next level  


---

### 🧭 Quick Action Summary  

- Login as `bandit18`  
- Run `cat readme` directly via SSH  
- Capture the output before the session closes  
- Obtain the password  


---

### 🔑 Credentials Provided  

- **Username:** bandit18  
- **Password:** x2gLTTjFwMOHQ80WNbMN36ZQKxFrQGIO  


---

### 🔍 Method of Solve  

The `bandit18` account is configured to immediately log out after login.  
However, SSH allows a command to be executed at the time of login.

Steps followed:  
- Connect via SSH  
- Execute `cat readme` as part of the SSH command  
- Read the output before logout  


---

### 🧪 Commands Used  

- `ssh bandit18@bandit.labs.overthewire.org -p 2220 cat readme`  


---

### 🧩 Command Purpose  

| Command | Purpose |
|--------|--------|
| `ssh ... cat readme` | Executes a command remotely during login |


---

### 📸 Screenshot Evidence  

![Bandit Level 18 Screenshot](screenshots/level18.png)


---

### 🔑 Next Level Password  

```
cGWpMaKXWDUNpPAJwbYUGHv9szJ3j8
```


---

### 🧠 Explanation  

- The SSH command runs `cat readme` before the shell is closed  
- The command output is printed even though the session ends  
- The output contains the password for the next level  


---

### 🔐 Concept Learned  

This level demonstrates remote command execution via SSH.  
It shows how restricted shells can sometimes be bypassed by executing commands during login.


---

### 🛡️ Security Insight  

Restricting interactive shells alone is not enough.  
Command execution during login should also be controlled to prevent information leakage.
