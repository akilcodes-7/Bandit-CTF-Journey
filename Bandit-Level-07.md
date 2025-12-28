## Bandit Level 07 → Level 08


### 🎯 Objective  

- Log in as `bandit7`  
- Locate the `data.txt` file  
- Extract the readable string that contains the password  
- Retrieve the password for the next level  


---

### 🧭 Quick Action Summary  

- Login as `bandit7`  
- Identify the `data.txt` file  
- Extract readable strings  
- Filter the line containing the keyword  
- Obtain the password  


---

### 🔑 Credentials Provided  

- **Username:** bandit7  
- **Password:** morbnDTkSW6jILucyDmQdM4LnOlfVAaj  


---

### 🔍 Method of Solve  

The password for the next level is hidden inside a file named `data.txt`.  
The file contains many unreadable characters, but the correct password appears as a readable string next to a specific keyword.

Steps followed:  
- List the files  
- Extract all readable strings  
- Filter the output using a keyword  
- Identify the password  


---

### 🧪 Commands Used  

- `ls -alph`  
- `strings data.txt | grep "millionth"`  


---

### 🧩 Command Purpose  

| Command | Purpose |
|--------|--------|
| `ls -alph` | Lists all files including hidden ones |
| `strings data.txt` | Extracts human-readable text from a file |
| `grep "millionth"` | Filters the output to show only the matching line |


---

### 📸 Screenshot Evidence  

![Bandit Level 07 Screenshot](screenshots/level07.png)


---

### 🔑 Next Level Password  

```
dfwvzFQi4mU0wfNbF0e9RoWskmLg7eEc
```


---

### 🧠 Explanation  

- The `strings` command extracts readable content from a file that contains binary data  
- The `grep "millionth"` filter isolates the line that contains the required keyword  
- That line includes the password for the next level  


---

### 🔐 Concept Learned  

This level demonstrates how readable information can be extracted from complex files.  
It highlights the effectiveness of command pipelines and filtering tools for data discovery.


---

### 🛡️ Security Insight  

Sensitive information embedded in binary or mixed files can still be recovered.  
Security reviews should include scanning such files to prevent hidden data leaks.
