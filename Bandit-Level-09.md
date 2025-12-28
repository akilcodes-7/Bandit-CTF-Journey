## Bandit Level 09 → Level 10


### 🎯 Objective  

- Log in as `bandit9`  
- Locate the `data.txt` file  
- Identify the readable string containing multiple `=` characters  
- Retrieve the password for the next level  


---

### 🧭 Quick Action Summary  

- Login as `bandit9`  
- Extract readable strings from `data.txt`  
- Filter lines containing `=`  
- Identify the password  


---

### 🔑 Credentials Provided  

- **Username:** bandit9  
- **Password:** 4CKMh1JI91bUIZZPXDqGana4vxAg0JM  


---

### 🔍 Method of Solve  

The password for the next level is hidden inside the `data.txt` file.  
The file contains binary data, but the password appears as a readable string that includes multiple equals (`=`) characters.

Steps followed:  
- Extract all readable strings  
- Filter strings containing `=`  
- Identify the correct password  


---

### 🧪 Commands Used  

- `strings data.txt | grep -e "="`  


---

### 🧩 Command Purpose  

| Command | Purpose |
|--------|--------|
| `strings data.txt` | Extracts readable text from a binary or mixed file |
| `grep -e "="` | Filters lines that contain the `=` character |


---

### 📸 Screenshot Evidence  

![Bandit Level 09 Screenshot](screenshots/level09.png)


---

### 🔑 Next Level Password  

```
FGUW5iLLvJrXx9kMYMnlN4MgbpfMiqey
```


---

### 🧠 Explanation  

- The `strings` command extracts human-readable text from the file  
- The `grep -e "="` filter isolates strings that contain repeated equals signs  
- One of these strings contains the password for the next level  


---

### 🔐 Concept Learned  

This level shows how to extract meaningful data from binary or mixed-content files.  
It demonstrates the power of pattern matching when searching for hidden credentials.


---

### 🛡️ Security Insight  

Credentials hidden inside binary files can still be recovered using string analysis.  
Security controls should ensure that sensitive data is not stored in unprotected files.
