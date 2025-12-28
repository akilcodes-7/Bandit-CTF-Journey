## Bandit Level 04 → Level 05


### 🎯 Objective  

- Log in as `bandit4`  
- Enter the `inhere` directory  
- Identify the readable ASCII file  
- Read the file to obtain the password for the next level  


---

### 🧭 Quick Action Summary  

- Login as `bandit4`  
- Navigate to the `inhere` directory  
- Scan all files to find the ASCII text file  
- Open the correct file to get the password  


---

### 🔑 Credentials Provided  

- **Username:** bandit4  
- **Password:** 2WmrDFRmJIq3IPxneAaMGhap0pFhS3NJ  


---

### 🔍 Method of Solve  

The password for the next level is hidden inside one readable ASCII file among many files of different types.  
Linux file identification tools are used to locate the correct file.

Steps followed:  
- Navigate to the `inhere` directory  
- List all files  
- Identify file types  
- Open the readable file  


---

### 🧪 Commands Used  

- `ls`  
- `cd inhere`  
- `ls -alph`  
- `find . -type f | xargs file`  
- `cat ./-file07`  


---

### 🧩 Command Purpose  

| Command | Purpose |
|--------|--------|
| `ls` | Lists files in the current directory |
| `cd inhere` | Moves into the `inhere` directory |
| `ls -alph` | Shows all files with detailed information |
| `find . -type f \| xargs file` | Identifies the type of each file |
| `cat ./-file07` | Reads the ASCII text file containing the password |


---

### 📸 Screenshot Evidence  

![Bandit Level 04 Screenshot](screenshots/level04.png)


---

### 🔑 Next Level Password  

```
koReBOKuIDDepwhWk7jZC0RTdopnAYKh
```


---

### 🧠 Explanation  

- The `inhere` directory contains multiple files of different types  
- The `find` and `file` commands identify which file contains readable ASCII text  
- The file `-file07` is the only readable text file  
- Reading this file reveals the password for the next level  


---

### 🔐 Concept Learned  

This level demonstrates how to analyze file types to locate meaningful data.  
It highlights the importance of filtering readable files when working with mixed file collections.


---

### 🛡️ Security Insight  

Sensitive data hidden among binary files may be overlooked during weak inspections.  
Proper file-type analysis is essential for accurate security assessments.
