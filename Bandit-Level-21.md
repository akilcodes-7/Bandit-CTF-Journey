## Bandit Level 21 → Level 22

### 🎯 Objective
Log in to the Bandit game as bandit21 and obtain the password for the next level by analyzing a cron job.

---

### 🔑 Credentials Provided
Username: bandit21  
Password: Obtained from previous level  

---

### 🔍 Method of Solve
A cron job runs periodically as bandit22. By inspecting the cron configuration and the script it executes, the location where the password is written can be found and read.

---

### 🧪 Commands Used
- cd /etc/cron.d  
- ls -la  
- cat cronjob_bandit22  
- cat /usr/bin/cronjob_bandit22.sh  
- cat /tmp/t706lds9S0Rq9h9aMcz6ShpAoZKF7fgv  

---

### 📸 Screenshot
![Bandit Level 21 Screenshot](screenshots/level21.png)

---

### 🔑 Next Level Password
tRae0ufB9v0JzbCd9cY0gQnds9GF58Q

---

### 🧠 Explanation
The cron configuration file `cronjob_bandit22` shows that a script is executed every minute as bandit22.  
Reading `/usr/bin/cronjob_bandit22.sh` reveals that the script copies the bandit22 password into a file inside `/tmp`.  
By reading that file, the password for the next level is obtained.

---

### 🔐 Concept Learned
This level demonstrates cron job analysis.  
It shows how scheduled tasks can expose sensitive data if temporary files are improperly protected.
