## Bandit Level 10 → Level 11


### 🎯 Objective  

- Log in as `bandit10`  
- Locate the Base64-encoded file  
- Decode the file  
- Retrieve the password for the next level  


---

### 🧭 Quick Action Summary  

- Login as `bandit10`  
- Identify `data.txt`  
- Decode the file using Base64  
- Extract the password  


---

### 🔑 Credentials Provided  

- **Username:** bandit10  
- **Password:** FGUW5iLLvJrXx9kMYMnlN4MgbpfMiqey  


---

### 🔍 Method of Solve  

The password for the next level is stored in a file named `data.txt`.  
This file is encoded using Base64, which must be decoded to reveal the original plaintext password.

Steps followed:  
- List the files  
- Decode the Base64 content  
- Read the decoded output  


---

### 🧪 Commands Used  

- `ls -alph`  
- `base64 -d data.txt`  


---

### 🧩 Command Purpose  

| Command | Purpose |
|--------|--------|
| `ls -alph` | Lists all files including hidden ones |
| `base64 -d data.txt` | Decodes the Base64-encoded file |


---

### 📸 Screenshot Evidence  

![Bandit Level 10 Screenshot](screenshots/level10.png)


---

### 🔑 Next Level Password  

```
dtR173fZKb0RRSDFSgsq2RwhpNVj3qR
```


---

### 🧠 Explanation  

- The file `data.txt` contains Base64-encoded data  
- The `base64 -d` command decodes the content back to its original form  
- The decoded output contains the password for the next level  


---

### 🔐 Concept Learned  

This level demonstrates how encoded data can be decoded using standard Linux utilities.  
It highlights the importance of recognizing common encoding formats such as Base64 during security analysis.


---

### 🛡️ Security Insight  

Encoding is not encryption.  
Sensitive data stored in encoded form can be easily decoded and exposed if not properly protected.
