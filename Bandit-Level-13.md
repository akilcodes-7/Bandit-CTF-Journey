## Bandit Level 13 → Level 14

### 🎯 Objective
Log in to the Bandit game as bandit13 and obtain the password for the next level by using an SSH private key instead of a normal password.

---

### 🔑 Credentials Provided
Username: bandit13  
Password: Obtained from previous level  

---

### 🔍 Method of Solve
The password for the next level is not provided directly. Instead, an SSH private key is given. This key must be used to authenticate as bandit14. After logging in, the password for bandit14 can be retrieved from a system file.

---

### 🧪 Commands Used
- scp -P 2220 bandit13@bandit.labs.overthewire.org:/home/bandit13/sshkey.private  
- chmod 600 sshkey.private  
- ssh -i sshkey.private bandit14@bandit.labs.overthewire.org -p 2220  
- cd /etc/bandit_pass  
- cat bandit14  

---

### 📸 Screenshots

**Step 1 – Private Key Extraction from Bandit Server**  
![Bandit Level 13 Screenshot – Server](screenshots/level13_1.png)

---

**Step 2 – SSH Login Using Private Key**  
![Bandit Level 13 Screenshot – SSH Login](screenshots/level13_2.png)

---

### 🔑 Next Level Password
MUuVWzTyJk8ROoFIgmgcBPaJh7LDCpVs

---

### 🧠 Explanation
The `scp` command securely copies the private SSH key from the Bandit server to the local Kali machine.  
The `-P 2220` option specifies the port used by the Bandit server.

The `chmod 600 sshkey.private` command restricts access to the private key so only the owner can read or modify it. SSH will refuse to use a key if it is accessible by others.

The `ssh -i sshkey.private bandit14@bandit.labs.overthewire.org -p 2220` command authenticates the user as bandit14 using the private key instead of a password.

Once logged in, `cd /etc/bandit_pass` navigates to the directory where Bandit stores passwords.  
The `cat bandit14` command displays the password for the next level.

---

### 🔐 Concept Learned
This level introduces SSH key-based authentication.  
It shows how private keys can be used for secure, passwordless login, which is widely used in real-world system administration and penetration testing.
