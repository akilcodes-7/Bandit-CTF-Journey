## Bandit Level 29 → Level 30

### 🎯 Objective
Log in to the Bandit game as bandit29 and obtain the password for the next level by examining a different branch of a Git repository.

---

### 🔑 Credentials Provided
Username: bandit29-git  
Password: Obtained from previous level  

---

### 🔍 Method of Solve
The password for the next level is not stored in the main branch of the repository. Instead, it is hidden in a different branch named `dev`. By switching to this branch and checking the commit history, the password can be recovered.

---

### 🧪 Commands Used
- git clone ssh://bandit29-git@bandit.labs.overthewire.org:2220/home/bandit29-git/repo  
- cd repo  
- cat README.md  
- git branch  
- git branch -a  
- git checkout dev  
- git log -p  

---

### 📸 Screenshots

**Cloning the Repository and Checking Available Branches**

![Bandit Level 29 – Repository](screenshots/level29_1.png)

---

**Viewing the Commit History in the Dev Branch to Reveal the Password**

![Bandit Level 29 – Dev Branch Commit](screenshots/level29_2.png)

---

### 🔑 Next Level Password
qp30ex3VLz5MDG1n91YovTv4Q81TCDZL

---

### 🧠 Explanation
The `git clone` command downloads the private repository for bandit29 over SSH.  
The `cat README.md` command shows that the password is hidden.  
The `git branch` and `git branch -a` commands list all local and remote branches, revealing the `dev` branch.  
The `git checkout dev` command switches to the development branch.  
The `git log -p` command displays the commit history and file differences, where the password is revealed in a previous version of the README file.

---

### 🔐 Concept Learned
This level demonstrates how Git branches can store different versions of data.  
It shows that sensitive information can exist in other branches even if it is removed from the main branch, highlighting the importance of checking all branches during security audits.
