## Bandit Level 05 → Level 06


### 🎯 Objective  

- Log in as `bandit5`  
- Search the `inhere` directory tree  
- Identify the file that matches the given size and permission conditions  
- Read the file to obtain the password for the next level  


---

### 🧭 Quick Action Summary  

- Login as `bandit5`  
- Move into the `inhere` directory  
- Find the file that is 1033 bytes, readable, and not executable  
- Read the file to get the password  


---

### 🔑 Credentials Provided  

- **Username:** bandit5  
- **Password:** 4oQYVPkxZ0OEOO5pTW81FB8j8lxXGUQw 


---

### 🔍 Method of Solve  

The password for the next level is stored inside a file that meets three conditions:  
it is human-readable, exactly 1033 bytes in size, and not executable.  
The file is located somewhere inside the `inhere` directory tree.

Steps followed:  
- Navigate into the `inhere` directory  
- Use file search filters to locate the correct file  
- Read the file once it is found  


---

### 🧪 Commands Used  

- `ls -alph`  
- `cd inhere`  
- `find . -type f -size 1033c ! -executable`  
- `cat ./maybehere07/.file2`  


---

### 🧩 Command Purpose  

| Command | Purpose |
|--------|--------|
| `ls -alph` | Displays all files including hidden ones with permissions |
| `cd inhere` | Moves into the `inhere` directory |
| `find . -type f -size 1033c ! -executable` | Searches for a non-executable file of exactly 1033 bytes |
| `cat ./maybehere07/.file2` | Reads the matched file containing the password |


---

### 📸 Screenshot Evidence  

![Bandit Level 05 Screenshot](screenshots/level05.png)


---

### 🔑 Next Level Password  

```
HWasnPhtq9AVKe0dmk5nx2oC6U6aBG
```


---

### 🧠 Explanation  

- The `find` command is used with size and permission filters to narrow down the search  
- Only one file satisfies all the required conditions  
- The file `.file2` inside `maybehere07` contains the correct password  
- Reading this file reveals the credentials for the next level  


---

### 🔐 Concept Learned  

This level demonstrates advanced file searching using size and permission filters.  
It shows how combining multiple conditions makes it possible to efficiently locate specific data in large directory structures.


---

### 🛡️ Security Insight  

Sensitive data can be hidden in large file systems using specific attributes such as size and permissions.  
Security reviews should include detailed file analysis to detect such hidden information.
