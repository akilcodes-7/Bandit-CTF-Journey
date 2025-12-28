## Bandit Level 02 → Level 03


### 🎯 Objective  

- Log in as `bandit2`  
- Locate the file that contains spaces in its name  
- Read the file to obtain the password for the next level  


---

### 🧭 Quick Action Summary  

- Login as `bandit2`  
- Identify the filename with spaces  
- Escape the spaces correctly  
- Read the file to extract the password  


---

### 🔑 Credentials Provided  

- **Username:** bandit2  
- **Password:** 263JGJPfgU6LtdEvfgWU1XP5yac29mFx  


---

### 🔍 Method of Solve  

The password for the next level is stored inside a file whose name contains spaces.  
Because spaces are treated as separators in Linux, they must be escaped or handled carefully to access the file.

Steps followed:  
- List all files in the directory  
- Identify the file with spaces in its name  
- Use proper escaping to read the file  


---

### 🧪 Commands Used  

- `ls`  
- `cat -- --spaces\ in\ this\ filename--`  


---

### 🧩 Command Purpose  

| Command | Purpose |
|--------|--------|
| `ls` | Displays all files in the current directory |
| `cat -- --spaces\ in\ this\ filename--` | Reads a file with spaces in its name by escaping them correctly |


---

### 📸 Screenshot Evidence  

![Bandit Level 02 Screenshot](screenshots/level02.png)


---

### 🔑 Next Level Password  

```
MNk8KNH3Usi14PLUODpFqfxLP1Smx
```


---

### 🧠 Explanation  

- The `ls` command shows a file whose name contains spaces  
- Backslashes (`\`) are used to escape the spaces so the shell treats the filename as a single string  
- This allows the file to be opened and read correctly  


---

### 🔐 Concept Learned  

This level demonstrates how Linux handles filenames that contain spaces.  
It highlights the importance of escaping special characters to prevent command misinterpretation.


---

### 🛡️ Security Insight  

Improper handling of filenames with spaces can lead to incorrect file access or command errors.  
Using proper escaping ensures reliable and secure file operations.
