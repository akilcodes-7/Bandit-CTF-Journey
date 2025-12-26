## Bandit Level 17 → Level 18

### 🎯 Objective
Log in to the Bandit game as bandit17 and obtain the password for the next level by comparing two password files.

---

### 🔑 Credentials Provided
Username: bandit17  
Password: Obtained from previous level  

---

### 🔍 Method of Solve
Two files, `passwords.new` and `passwords.old`, contain different versions of passwords. By comparing them, the newly added password can be identified and used for the next level.

---

### 🧪 Commands Used
- ls  
- diff passwords.new passwords.old  

---

### 📸 Screenshot
![Bandit Level 17 Screenshot](screenshots/level17.png)

---

### 🔑 Next Level Password
BMIOFKM7CRSLI97volp3TD80NAq5exxk

---

### 🧠 Explanation
The `ls` command lists all files in the directory and shows the two password files.  
The `diff` command compares both files line by line and highlights differences.  
Lines starting with `>` indicate content present only in `passwords.new`, which reveals the new password for the next level.

---

### 🔐 Concept Learned
This level demonstrates file comparison using the `diff` command.  
It shows how differences between file versions can be identified, a common technique in system administration and security analysis.
