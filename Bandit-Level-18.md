## Bandit Level 18 → Level 19

### 🎯 Objective
Log in to the Bandit game as bandit18 and obtain the password for the next level even though the shell immediately logs out.

---

### 🔑 Credentials Provided
Username: bandit18  
Password: Obtained from previous level  

---

### 🔍 Method of Solve
The Bandit18 account is configured to log out immediately after login.  
However, SSH allows commands to be executed directly during login. By running `cat readme` through SSH, the password can be retrieved before the session closes.

---

### 🧪 Commands Used
- ssh bandit18@bandit.labs.overthewire.org -p 2220 cat readme  

---

### 📸 Screenshot
![Bandit Level 18 Screenshot](screenshots/level18.png)

---

### 🔑 Next Level Password
cGWpMaKXWvDUNGpAVJbWYUGHVN9z1J38

---

### 🧠 Explanation
The `ssh` command is used to connect to the Bandit server.  
By appending `cat readme` at the end of the SSH command, the command is executed immediately after login.  
Even though the shell logs out instantly, the command runs and prints the contents of the `readme` file, which contains the password for the next level.

---

### 🔐 Concept Learned
This level demonstrates how remote command execution can be performed through SSH.  
It shows how restricted shells can sometimes be bypassed by running commands directly during the login process.
