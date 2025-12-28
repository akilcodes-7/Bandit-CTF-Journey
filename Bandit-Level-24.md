## Bandit Level 24 → Level 25

### 🎯 Objective
Log in to the Bandit game as bandit24 and obtain the password for the next level by brute-forcing a 4-digit PIN required by a local network service.

---

### 🔑 Credentials Provided
Username: bandit24  
Password: Obtained from previous level  

---

### 🔍 Method of Solve
A daemon running on localhost port `30002` requires the current password and a 4-digit PIN to authenticate.  
Since the PIN space is small (0000–9999), a brute-force attack can be performed using a Python script to test all possible PIN combinations until the correct one is found.

---

### 🧪 Commands Used
- cd /tmp/ak  
- ls -la  
- nano ...ak.py  
- python3 ...ak.py  

---

### 📸 Screenshots

**Step 1 – Creating the Python Brute-Force Script**  

![Bandit Level 24 – Python Script](screenshots/level24_1.png)

---

**Step 2 – Successful PIN Brute-Force and Password Retrieval**  

![Bandit Level 24 – Password Found](screenshots/level24_2.png)

---

### 🔑 Next Level Password
iCi8ttT4KSNe1armKiwbQNmB3YJP3g4

---

### 🧠 Explanation
The Python script opens a new socket connection to `127.0.0.1` on port `30002` for each PIN attempt.  
For every value from `0000` to `9999`, it sends the current password along with the PIN.

The service responds with `"Wrong"` for incorrect attempts.  
When the correct PIN is sent, the response changes and returns the password for bandit25.

The script detects this success condition and prints both the valid PIN and the next level password.

---

### 🔐 Concept Learned
This level demonstrates controlled brute-force attacks against network services.  
It highlights how limited key spaces can be exploited programmatically and reinforces the importance of rate-limiting and lockout mechanisms in secure systems.
