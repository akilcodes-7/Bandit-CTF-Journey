## Bandit Level 19 → Level 20

### 🎯 Objective
Log in to the Bandit game as bandit19 and obtain the password for the next level by using a special executable file.

---

### 🔑 Credentials Provided
Username: bandit19  
Password: Obtained from previous level  

---

### 🔍 Method of Solve
A file named `bandit20-do` is a set-UID executable owned by bandit20.  
When executed, it runs commands with the privileges of bandit20.  
This allows reading the password file of bandit20.

---

### 🧪 Commands Used
- ls -la  
- ./bandit20-do cat /etc/bandit_pass/bandit20  

---

### 📸 Screenshot
![Bandit Level 19 Screenshot](screenshots/level19.png)

---

### 🔑 Next Level Password
0qXahG8ZJOVMNGhs7iOWsCfZyXOUbY0

---

### 🧠 Explanation
The `ls -la` command lists all files and shows file permissions.  
The file `bandit20-do` has the set-UID bit enabled, meaning it runs with the permissions of its owner (bandit20).

Running `./bandit20-do cat /etc/bandit_pass/bandit20` executes the `cat` command as bandit20, allowing access to bandit20’s password file and revealing the next level password.

---

### 🔐 Concept Learned
This level demonstrates the use of **set-UID binaries**.  
It shows how programs can temporarily run with higher privileges, a concept that is critical in Linux privilege escalation and system security.
