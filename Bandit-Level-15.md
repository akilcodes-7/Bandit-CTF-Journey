## Bandit Level 15 → Level 16

### 🎯 Objective
Log in to the Bandit game as bandit15 and obtain the password for the next level by connecting to a secure SSL-enabled service.

---

### 🔑 Credentials Provided
Username: bandit15  
Password: Obtained from previous level  

---

### 🔍 Method of Solve
A secure service is running on port 30001 on localhost. The current password must be sent to this service over an SSL-encrypted connection to receive the next level password.

---

### 🧪 Commands Used
- ncat --ssl localhost 30001  

---

### 📸 Screenshot
![Bandit Level 15 Screenshot](screenshots/level15.png)

---

### 🔑 Next Level Password
kSkvUpMQ7LByVCM4GBPvCvT1BfWRy0Dx

---

### 🧠 Explanation
The `ncat --ssl localhost 30001` command establishes an encrypted SSL connection to the local service running on port 30001.  
Once connected, the current password is sent securely to the service.  
The service verifies the password and returns the password for the next Bandit level.

---

### 🔐 Concept Learned
This level introduces secure network communication using SSL.  
It demonstrates how encryption protects data while it is transmitted over a network, a critical concept in secure system administration and penetration testing.
