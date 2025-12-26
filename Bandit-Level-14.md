## Bandit Level 14 → Level 15

### 🎯 Objective
Log in to the Bandit game as bandit14 and obtain the password for the next level by sending the current password to a service running on localhost.

---

### 🔑 Credentials Provided
Username: bandit14  
Password: Obtained from previous level  

---

### 🔍 Method of Solve
A network service is running on port 30000 of the local machine. By sending the current password to this service using a network connection, the server returns the password for the next level.

---

### 🧪 Commands Used
- nc localhost 30000  

---

### 📸 Screenshot
![Bandit Level 14 Screenshot](screenshots/level14.png)

---

### 🔑 Next Level Password
8xCjmmoKp6GLLhHFAZIG5Tmu4M2tKJQO

---

### 🧠 Explanation
The `nc` (Netcat) command is used to create a TCP connection to the local service running on port 30000.  
After connecting, the current level password is entered.  
The service verifies the password and returns the password for the next level as a response.

---

### 🔐 Concept Learned
This level introduces basic network communication using Netcat.  
It demonstrates how services can accept input over a network connection and respond with sensitive information, a common technique used in penetration testing and service enumeration.
