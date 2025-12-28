## Bandit Level 00 → Level 01


### 🎯 Objective  

- Log in to the Bandit game using the given credentials  
- Read the `readme` file  
- Obtain the password for the next level  


---

### 🧭 Quick Action Summary  

- Login as `bandit0`  
- Locate the `readme` file  
- Read the file to extract the password  
- Use the password to access the next level  


---

### 🔑 Credentials Provided  

- **Username:** bandit0  
- **Password:** bandit0  


---

### 🔍 Method of Solve  

The password for the next level is stored inside a file named `readme` in the home directory.  
By listing the files and reading the contents of this file, the password can be obtained.

Steps followed:  
- Display the list of files  
- Open and read the `readme` file  


---

### 🧪 Commands Used  

- `ls`  
- `cat readme`  


---

### 🧩 Command Purpose  

| Command | Purpose |
|--------|--------|
| `ls` | Lists all files in the current directory |
| `cat readme` | Displays the contents of the `readme` file |


---

### 📸 Screenshot Evidence  

![Bandit Level 00 Screenshot](screenshots/level00.png)


---

### 🔑 Next Level Password  

```
ZjlJTmM6FvvyRnrB2rfNWOZOTa6ip5If
```


---

### 🧠 Explanation  

- The `ls` command is used to view the files present in the directory  
- The `cat readme` command outputs the contents of the `readme` file  
- The displayed content contains the password required for the next Bandit level  


---

### 🔐 Concept Learned  

This level introduces basic Linux command-line operations:  
- Navigating directories  
- Viewing file contents  
- Understanding how sensitive data can be stored inside files  

It highlights how simple commands can be used to access important system information.


---

### 🛡️ Security Insight  

Storing passwords in plain text files is insecure.  
If file permissions are misconfigured, unauthorized users could read sensitive data and compromise system security.
