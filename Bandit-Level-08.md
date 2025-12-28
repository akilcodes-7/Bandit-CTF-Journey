## Bandit Level 08 → Level 09


### 🎯 Objective  

- Log in as `bandit8`  
- Locate the `data.txt` file  
- Identify the unique line  
- Retrieve the password for the next level  


---

### 🧭 Quick Action Summary  

- Login as `bandit8`  
- Sort the contents of `data.txt`  
- Count duplicate lines  
- Find the line that appears only once  
- Extract the password  


---

### 🔑 Credentials Provided  

- **Username:** bandit8  
- **Password:** dfwvzFQi4mU0wfNbF0e9RoWskmLg7eEc  


---

### 🔍 Method of Solve  

The password for the next level is stored inside a file named `data.txt`.  
The file contains many duplicate lines, and the correct password is the only line that appears once.

Steps followed:  
- List the files  
- Sort all lines in the file  
- Count the occurrences of each line  
- Identify the unique line  


---

### 🧪 Commands Used  

- `ls -alph`  
- `sort data.txt | uniq -c`  


---

### 🧩 Command Purpose  

| Command | Purpose |
|--------|--------|
| `ls -alph` | Displays all files including hidden ones |
| `sort data.txt` | Sorts all lines in the file |
| `uniq -c` | Counts the number of occurrences of each line |


---

### 📸 Screenshot Evidence  

![Bandit Level 08 Screenshot](screenshots/level08.png)


---

### 🔑 Next Level Password  

```
4CKMh1JI91bUIZZPXDqGana4vxAg0JM
```


---

### 🧠 Explanation  

- The `sort` command arranges all lines alphabetically  
- The `uniq -c` command counts how many times each line appears  
- The line with a count of `1` is the unique entry and contains the password  


---

### 🔐 Concept Learned  

This level demonstrates how to analyze repeated data using sorting and filtering.  
It shows how text-processing tools can be combined to extract meaningful information.


---

### 🛡️ Security Insight  

Duplicate data can hide critical information.  
Using counting and filtering techniques helps reveal hidden or unique entries in large datasets.
