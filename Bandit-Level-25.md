## Bandit Level 25 → Level 26

### 🎯 Objective
Log in to the Bandit game as bandit25 and obtain the password for the next level by escaping the restricted shell used by bandit26.

---

### 🔑 Credentials Provided
Username: bandit25  
Password: Obtained from previous level  

---

### 🔍 Method of Solve
The bandit26 account does not use a normal Bash shell. Instead, it runs a script that displays text using the `more` pager.  
By forcing `more` into interactive mode and escaping into Vim, a real Bash shell can be spawned to read the password.

---

### 🧪 Commands Used
- ls  
- file bandit26.sshkey  
- scp -P 2220 bandit25@bandit.labs.overthewire.org:/home/bandit25/bandit26.sshkey .  
- chmod 600 bandit26.sshkey  
- ssh -i bandit26.sshkey bandit26@bandit.labs.overthewire.org -p 2220  
- v  
- :set shell=/bin/bash  
- :shell  
- cat /etc/bandit_pass/bandit26  

---

### 📸 Screenshots

**Step 1 – Locating the SSH Private Key**  

![Bandit Level 25 – Key Found](screenshots/level25_1.png)

---

**Step 2 – Copying the Key Using SCP**  

![Bandit Level 25 – SCP Transfer](screenshots/level25_2.png)

---

**Step 3 – Logging in and Triggering the `more` Pager**  

![Bandit Level 25 – Restricted Shell](screenshots/level25_3.png)

---

**Step 4 – Escaping to Vim and Opening a Bash Shell**

![Bandit Level 25 – Vim Escape](screenshots/level25_4.png)

---

**Step 5 – Reading the Next Level Password**  

![Bandit Level 25 – Password](screenshots/level25_5.png)

---

### 🔑 Next Level Password
s07r3xxk0MXfdq0fPrv9L3jJBUOgCZ

---

### 🧠 Explanation
The SSH private key allows logging in as bandit26, but the account runs a restricted program that displays text using the `more` pager.

To force `more` into interactive mode, the terminal window is intentionally made small so that the text does not fit on one screen.  
This causes `more` to pause and wait for input.

Pressing `v` inside `more` opens Vim.  
Inside Vim, `:set shell=/bin/bash` changes the shell, and `:shell` launches a real Bash shell.

Once full shell access is obtained, `cat /etc/bandit_pass/bandit26` reveals the password for the next level.

---

### 🔐 Concept Learned
This level demonstrates restricted shell bypassing.  
It shows how pager programs and text editors can be abused to escape sandboxed environments and gain full command-line access.
