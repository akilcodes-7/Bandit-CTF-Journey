## Bandit Level 26 → Level 27

---

### 🎯 Objective
Log in to the **bandit26** account using the SSH key.  
The shell of bandit26 is restricted and only shows a text file.  
Escape from this restricted environment, gain a real shell, and use the **bandit27-do** binary to read the password for the next level.

---

### 🔑 Credentials Provided
- **Username:** bandit26  
- **Login Method:** SSH Private Key  
- **SSH Key File:** `bandit26.sshkey`  

---

### 🔍 Method of Solve
Bandit26 does not give a normal shell. Instead, it opens a file using the `more` pager.  
By shrinking the terminal window, `more` pauses and allows entering **VIM**.  
From VIM, we can change the shell to `/bin/bash` and spawn a real shell.  
Once we have a shell, we use **bandit27-do**, which runs commands as bandit27, to read the password.

---

### 🧪 Commands Used
```bash
# Login to bandit26 using SSH key
ssh -i bandit26.sshkey bandit26@bandit.labs.overthewire.org -p 2220

# When the text file opens in "more", press:
v

# Inside VIM, set a real shell
:set shell=/bin/bash

# Spawn the shell
:shell

# Check available files
ls

# Use bandit27-do to read bandit27 password
./bandit27-do cat /etc/bandit_pass/bandit27
```

---

### 📸 Screenshots

![Login with SSH key](screenshots/level26_1.png)

---

![Restricted more shell](screenshots/level26_2.png)

---

![VIM shell escape](screenshots/level26_3.png)

---

![Using bandit27-do](screenshots/level26_4.png)

---

### 🔑 Next Level Password
```
upsNCc7vzaRDx60zC6GiR6EwRe1MowGB
```

---

### 🧠 Explanation
The bandit26 shell runs a script that displays a text file using `more`.  
When the terminal is small, `more` pauses output, allowing interactive commands.  
Pressing **v** opens the file in **VIM**.  
Inside VIM, the shell is changed to `/bin/bash`, allowing execution of real Linux commands.  
The `bandit27-do` binary allows running commands as bandit27, which is used to read the password file.

---

### 🔐 Concept Learned
This level demonstrates how interactive programs like `more` and `vim` can be abused to escape restricted shells.  
It also shows how **set-uid binaries** such as `bandit27-do` can be used to execute commands as another user.
