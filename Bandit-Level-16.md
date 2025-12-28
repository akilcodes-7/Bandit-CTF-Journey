## Bandit Level 16 → Level 17


### 🎯 Objective  

- Log in as `bandit16`  
- Connect to the secure SSL service  
- Retrieve the RSA private key  
- Use the key to log in as `bandit17`  
- Obtain the password for the next level  


---

### 🧭 Quick Action Summary  

- Login as `bandit16`  
- Connect to the SSL service on port `31790`  
- Save the RSA private key  
- Use the key to authenticate via SSH  
- Read the password file  


---

### 🔑 Credentials Provided  

- **Username:** bandit16  
- **Password:** kSkvUpMQ71BYvCM4GBPvCvT1BfWrQDx  


---

### 🔍 Method of Solve  

A secure SSL service provides an RSA private key.  
This key must be saved and used to authenticate as `bandit17` in order to retrieve the next level password.

Steps followed:  
- Connect to the SSL service  
- Save the RSA key to a file  
- Set correct file permissions  
- Use the key to log in via SSH  
- Read the password file  


---

### 🧪 Commands Used  

- `ncat --ssl localhost 31790`  
- `nano key17`  
- `chmod 600 key17`  
- `ssh -i key17 bandit17@bandit.labs.overthewire.org -p 2220`  
- `cd /etc/bandit_pass`  
- `cat bandit17`  


---

### 🧩 Command Purpose  

| Command | Purpose |
|--------|--------|
| `ncat --ssl localhost 31790` | Connects to the secure SSL service |
| `chmod 600 key17` | Secures the private key file |
| `ssh -i key17` | Logs in using the RSA private key |
| `cat bandit17` | Displays the password for the next level |


---

### 📸 Screenshot Evidence  

**Step 1 – RSA Private Key Received from SSL Service**  
![Bandit Level 16 – Key Received](screenshots/level16_1.png)

**Step 2 – Saving the RSA Private Key**  
![Bandit Level 16 – Key Saved](screenshots/level16_2.png)

**Step 3 – SSH Login Using Private Key**  
![Bandit Level 16 – SSH Login](screenshots/level16_3.png)

**Step 4 – Retrieving the Next Level Password**  
![Bandit Level 16 – Password](screenshots/level16_4.png)


---

### 🔑 Next Level Password  

```
EReVavePLFHTflsjnhyZmIvsuSaCRD
```


---

### 🧠 Explanation  

- The SSL service outputs an RSA private key  
- The key is saved and secured with correct permissions  
- The key is used to authenticate as `bandit17`  
- The password is retrieved from the system directory  


---

### 🔐 Concept Learned  

This level combines SSL communication and SSH key-based authentication.  
It demonstrates how encrypted key transfer enables secure system access.


---

### 🛡️ Security Insight  

Private keys must be protected at all times.  
If compromised, attackers can gain direct access without needing passwords.
