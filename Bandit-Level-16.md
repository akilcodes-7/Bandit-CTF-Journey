## Bandit Level 16 → Level 17

### 🎯 Objective
Log in to the Bandit game as bandit16 and obtain the password for the next level by identifying a secure service, extracting an RSA private key, and using it to authenticate.

---

### 🔑 Credentials Provided
Username: bandit16  
Password: Obtained from previous level  

---

### 🔍 Method of Solve
A secure SSL service running on localhost provides an RSA private key. This key must be retrieved, saved locally, and used to log in to bandit17. After successful login, the password for the next level is stored in the system.

---

### 🧪 Commands Used
- ncat --ssl localhost 31790  
- nano key17  
- chmod 600 key17  
- ssh -i key17 bandit17@bandit.labs.overthewire.org -p 2220  
- cd /etc/bandit_pass  
- cat bandit17  

---

### 📸 Screenshots

**Step 1 – RSA Private Key Received from SSL Service**  
![Bandit Level 16 – Key Received](screenshots/level16_1.png)

---

**Step 2 – Saving the RSA Private Key**  
![Bandit Level 16 – Key Saved](screenshots/level16_2.png)

---

**Step 3 – SSH Login Using Private Key**  
![Bandit Level 16 – SSH Login](screenshots/level16_3.png)

---

**Step 4 – Retrieving the Next Level Password**  
![Bandit Level 16 – Password](screenshots/level16_4.png)

---

### 🔑 Next Level Password
EREwEVPLHFtFlFSjn3hyzMlVsuSAcRD

---

### 🧠 Explanation
The `ncat --ssl localhost 31790` command connects to the secure SSL service that outputs an RSA private key.  
The key is copied and saved into a file named `key17`.

The `chmod 600 key17` command ensures that only the file owner can access the private key, which is required by SSH.

The `ssh -i key17 bandit17@bandit.labs.overthewire.org -p 2220` command logs into the Bandit server using the private key instead of a password.

Once logged in, the directory `/etc/bandit_pass` contains the password file for bandit17.  
The `cat bandit17` command displays the password for the next level.

---

### 🔐 Concept Learned
This level demonstrates SSL-encrypted communication and SSH key-based authentication.  
It highlights how private keys can be securely transmitted and then used to access protected systems without using passwords.
