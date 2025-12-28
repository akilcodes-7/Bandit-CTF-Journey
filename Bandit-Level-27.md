## Bandit Level 27 → Level 28

### 🎯 Objective
Log in to the Bandit game as bandit27 and obtain the password for the next level by accessing a private Git repository.

---

### 🔑 Credentials Provided
Username: bandit27-git  
Password: Obtained from previous level  

---

### 🔍 Method of Solve
The password for the next level is stored inside a private Git repository owned by bandit27. Instead of logging into a shell, the repository must be accessed over SSH using Git and then the stored file must be read.

---

### 🧪 Commands Used
- git clone ssh://bandit27-git@bandit.labs.overthewire.org:2220/home/bandit27-git/repo  
- cd repo  
- cat README  

---

### 📸 Screenshot
![Bandit Level 27 Screenshot](screenshots/level27.png)

---

### 🔑 Next Level Password
Yz9ipL0sBcCeuG7m9uQFt8zNpS4HZRcN

---

### 🧠 Explanation
The `git clone` command connects to the remote Git server using SSH and downloads the private repository belonging to bandit27.  
The `cd repo` command moves into the cloned repository directory.  
The `cat README` command displays the contents of the README file, which contains the password for the next Bandit level.

---

### 🔐 Concept Learned
This level demonstrates how private Git repositories can be accessed over SSH.  
It highlights how sensitive data can be stored inside version-controlled repositories and how Git can be used to retrieve information from remote servers securely.
