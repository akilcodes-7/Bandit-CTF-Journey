## Bandit Level 32 → Level 33

### 🎯 Objective
Log in to the Bandit game as bandit32 and obtain the password for the next level by escaping a restricted uppercase shell.

---

### 🔑 Credentials Provided
Username: bandit32  
Password: Obtained from previous level  

---

### 🔍 Method of Solve
Bandit32 provides a restricted shell that only accepts uppercase input. To execute normal Linux commands, an environment variable is used to escape the restricted shell and start a real Bash shell.

---

### 🧪 Commands Used
- $0  
- bash  
- cat /etc/bandit_pass/bandit33  

---

### 📸 Screenshot

**Escaping the Uppercase Shell and Reading the Password**
![Bandit Level 32 Screenshot](screenshots/level32.png)

---

### 🔑 Next Level Password
tQdtbs5D5i2vJwk08mEyYETL81z0eJ0

---

### 🧠 Explanation
The `$0` variable contains the name of the current shell. Executing `$0` runs a new instance of the shell without the uppercase restriction.  
The `bash` command starts a normal interactive Bash shell.  
The `cat /etc/bandit_pass/bandit33` command displays the password file for the next level.

---

### 🔐 Concept Learned
This level demonstrates how restricted shells can be bypassed using environment variables.  
It highlights the importance of understanding how shells work internally and how improper restrictions can be exploited.
