## Bandit Level 03 → Level 04


### 🎯 Objective  

- Log in as `bandit3`  
- Enter the `inhere` directory  
- Locate the hidden file  
- Read the file to obtain the password for the next level  


---

### 🧭 Quick Action Summary  

- Login as `bandit3`  
- Move into the `inhere` directory  
- List all files including hidden ones  
- Read the hidden file to extract the password  


---

### 🔑 Credentials Provided  

- **Username:** bandit3  
- **Password:** MNk8KNH3Usi14PLUODpFqfxLP1Smx  


---

### 🔍 Method of Solve  

The password for the next level is stored in a hidden file inside the `inhere` directory.  
Hidden files are not shown by default and must be listed using special options.

Steps followed:  
- Locate the `inhere` directory  
- Navigate into it  
- Display all files including hidden ones  
- Read the hidden file  


---

### 🧪 Commands Used  

- `ls`  
- `cd inhere`  
- `ls -alph`  
- `cat ...Hiding-From-You`  


---

### 🧩 Command Purpose  

| Command | Purpose |
|--------|--------|
| `ls` | Lists files and directories |
| `cd inhere` | Moves into the `inhere` directory |
| `ls -alph` | Shows all files, including hidden ones, with details |
| `cat ...Hiding-From-You` | Reads the hidden file to display its contents |


---

### 📸 Screenshot Evidence  

![Bandit Level 03 Screenshot](screenshots/level03.png)


---

### 🔑 Next Level Password  

```
2WmrDFRmJIq3IPxneAaMGhap0pFhS3NJ
```


---

### 🧠 Explanation  

- The `ls` command reveals the `inhere` directory  
- The `cd inhere` command moves into that directory  
- The `ls -alph` command displays all files, including hidden ones  
- The hidden file `...Hiding-From-You` contains the password for the next level  


---

### 🔐 Concept Learned  

This level demonstrates how hidden files are managed in Linux.  
It shows how command options can be used to reveal and access files that are not visible by default.


---

### 🛡️ Security Insight  

Hidden files can store sensitive data that is not immediately visible to users.  
Security checks should include scanning hidden files to prevent unauthorized data exposure.
