## Bandit Level 01 → Level 02


### 🎯 Objective  

- Log in as `bandit1`  
- Locate the file named `-`  
- Read the file to obtain the password for the next level  


---

### 🧭 Quick Action Summary  

- Login as `bandit1`  
- Identify the file named `-`  
- Access the file using a relative path  
- Extract the password for Level 02  


---

### 🔑 Credentials Provided  

- **Username:** bandit1  
- **Password:** ZjlJTmM6FvvyRnrB2rfNWOZOTa6ip5If  


---

### 🔍 Method of Solve  

The password for the next level is stored inside a file named `-`.  
Because filenames starting with a hyphen are treated as command options, the file must be accessed using a relative path.

Steps followed:  
- List all files in the directory  
- Use a relative path to safely open the file  
- Read the file to retrieve the password  


---

### 🧪 Commands Used  

- `ls`  
- `cat ./-`  


---

### 🧩 Command Purpose  

| Command | Purpose |
|--------|--------|
| `ls` | Lists all files in the current directory |
| `cat ./-` | Reads the file named `-` by treating it as a filename instead of an option |


---

### 📸 Screenshot Evidence  

![Bandit Level 01 Screenshot](screenshots/level01.png)


---

### 🔑 Next Level Password  

```
263JGJPfgU6LtdEvfgWU1XP5yac29mFx
```


---

### 🧠 Explanation  

- The `ls` command reveals a file named `-` in the directory  
- The `cat ./-` command forces the shell to treat `-` as a file  
- This allows the contents of the file to be displayed correctly  


---

### 🔐 Concept Learned  

This level demonstrates how Linux handles filenames that begin with special characters.  
It highlights why relative paths are required to avoid misinterpretation by the shell.


---

### 🛡️ Security Insight  

Files with special characters in their names can cause unexpected command behavior.  
Using explicit paths prevents accidental misuse and improves command reliability.
