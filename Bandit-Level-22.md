## Bandit Level 22 → Level 23

### 🎯 Objective
Log in to the Bandit game as bandit22 and obtain the password for the next level by analyzing a cron job.

---

### 🔑 Credentials Provided
Username: bandit22  
Password: Obtained from previous level  

---

### 🔍 Method of Solve
A cron job runs as bandit23 and stores the password in a dynamically named file inside `/tmp`.  
By reading the cron script, the filename generation logic can be reproduced to locate and read the password.

---

### 🧪 Commands Used
- cd /etc/cron.d  
- ls -la  
- cat cronjob_bandit23  
- cat /usr/bin/cronjob_bandit23.sh  
- echo I am user bandit23 | md5sum  
- cat /tmp/<md5_hash>  

---

### 📸 Screenshot
![Bandit Level 22 Screenshot](screenshots/level22.png)

---

### 🔑 Next Level Password
0Zflio1JmIVM551X3CmStKLyqiK54Ga

---

### 🧠 Explanation
The cron configuration shows that `/usr/bin/cronjob_bandit23.sh` runs every minute as bandit23.  
The script uses the command `whoami` and `md5sum` to generate a unique filename.  
By replicating this logic manually, the correct filename inside `/tmp` is determined.  
Reading that file reveals the password for the next level.

---

### 🔐 Concept Learned
This level demonstrates automated task analysis using cron jobs.  
It shows how predictable filename generation can expose sensitive information if proper security controls are not in place.
