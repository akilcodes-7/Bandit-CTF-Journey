## Bandit Level 20 → Level 21

### 🎯 Objective
Log in to the Bandit game as bandit20 and obtain the password for the next level by interacting with a set-UID network program.

---

### 🔑 Credentials Provided
Username: bandit20  
Password: Obtained from previous level  

---

### 🔍 Method of Solve
A program called `suconnect` runs as bandit21 and sends the next password to a service listening on a specified port.  
By running a Netcat listener and connecting `suconnect` to it, the password can be intercepted.

---

### 🧪 Commands Used
- nc -lvp 5000  
- ./suconnect 5000  

---

### 📸 Screenshot
![Bandit Level 20 Screenshot](screenshots/level20.png)

---

### 🔑 Next Level Password
EeoL1MCra2q0dSkYj561DX7s1CpBuOBt

---

### 🧠 Explanation
The `nc -lvp 5000` command starts a Netcat listener on port 5000 to wait for incoming connections.  
The `./suconnect 5000` command runs a set-UID program that connects to the given port and sends the next level password.  
When the program connects to the Netcat listener, the password is transmitted and displayed.

---

### 🔐 Concept Learned
This level demonstrates network-based privilege escalation.  
It shows how a privileged program can send sensitive data over a network connection, which can be intercepted by listening on the correct port.
