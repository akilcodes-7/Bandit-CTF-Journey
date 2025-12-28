## Bandit Level 11 → Level 12


### 🎯 Objective  

- Log in as `bandit11`  
- Locate the ROT13-encoded file  
- Decode the text  
- Retrieve the password for the next level  


---

### 🧭 Quick Action Summary  

- Login as `bandit11`  
- Open `data.txt`  
- Apply ROT13 decoding  
- Extract the password  


---

### 🔑 Credentials Provided  

- **Username:** bandit11  
- **Password:** dtR173fZKb0RRSDFSgsq2RwhpNVj3qR  


---

### 🔍 Method of Solve  

The password for the next level is stored inside a file named `data.txt`.  
The contents are encoded using the ROT13 substitution cipher, which shifts each letter by 13 positions.

Steps followed:  
- List the files  
- Read the encoded text  
- Apply ROT13 decoding  
- Read the decoded output  


---

### 🧪 Commands Used  

- `ls -alph`  
- `cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'`  


---

### 🧩 Command Purpose  

| Command | Purpose |
|--------|--------|
| `ls -alph` | Lists all files including hidden ones |
| `tr 'A-Za-z' 'N-ZA-Mn-za-m'` | Applies ROT13 decoding to the text |


---

### 📸 Screenshot Evidence  

![Bandit Level 11 Screenshot](screenshots/level11.png)


---

### 🔑 Next Level Password  

```
7x16WNeHIi5YkIHwsFF1QoognUTyj9Q4
```


---

### 🧠 Explanation  

- The file `data.txt` contains ROT13-encoded text  
- The `tr` command translates each character to its decoded form  
- The output reveals the password for the next level  


---
