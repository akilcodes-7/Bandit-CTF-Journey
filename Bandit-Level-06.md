## Bandit Level 06 → Level 07


### 🎯 Objective  

- Log in as `bandit6`  
- Search the entire filesystem  
- Locate the file that matches the given owner, group, and size  
- Read the file to obtain the password for the next level  


---

### 🧭 Quick Action Summary  

- Login as `bandit6`  
- Run a filtered `find` command  
- Ignore permission errors  
- Read the correct password file  


---

### 🔑 Credentials Provided  

- **Username:** bandit6  
- **Password:** HWasnPhtq9AVKe0dmk5nx2oC6U6aBG  


---

### 🔍 Method of Solve  

The password for the next level is stored in a file that meets three conditions:  
it is owned by user `bandit7`, belongs to group `bandit6`, and is exactly 33 bytes in size.  
The file exists somewhere on the system and must be located using a filtered search.

Steps followed:  
- Search the entire filesystem  
- Filter files by owner, group, and size  
- Ignore permission-denied messages  
- Open the matched file  


---

### 🧪 Commands Used  

- `ls -alph`  
- `find / -type f -user bandit7 -group bandit6 -size 33c`  
- `cat /var/lib/dpkg/info/bandit7.password`  


---

### 🧩 Command Purpose  

| Command | Purpose |
|--------|--------|
| `ls -alph` | Displays all files with permissions and hidden entries |
| `find / -type f -user bandit7 -group bandit6 -size 33c` | Searches the entire system for a file matching owner, group, and size |
| `cat /var/lib/dpkg/info/bandit7.password` | Reads the file that contains the password |


---

### 📸 Screenshot Evidence  

![Bandit Level 06 Screenshot](screenshots/level06.png)

![Bandit Level 06 Screenshot](screenshots/llevel06.png)


---

### 🔑 Next Level Password  

```
morbnDTkSW6jILucyDmQdM4LnOlfVAaj
```


---

### 🧠 Explanation  

- The `find` command scans the system with specific ownership and size filters  
- Permission denied messages are normal during system-wide searches  
- The correct file is found at `/var/lib/dpkg/info/bandit7.password`  
- Reading this file reveals the password for the next level  


---

### 🔐 Concept Learned  

This level demonstrates advanced file searching using user, group, and size constraints.  
It shows how targeted searches can locate sensitive files even in large system directories.


---

### 🛡️ Security Insight  

System configuration files may contain sensitive credentials.  
Restricting file ownership and permissions is essential to prevent unauthorized access.
