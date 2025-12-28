## Bandit Level 31 → Level 32

### 🎯 Objective
Log in to the Bandit game as bandit31 and obtain the password for the next level by pushing a file to a remote Git repository.

---

### 🔑 Credentials Provided
Username: bandit31-git  
Password: Obtained from previous level  

---

### 🔍 Method of Solve
The remote Git repository requires a specific file to be added and pushed. By creating the required file with the correct content, committing it, and pushing it to the remote repository, the server validates the submission and reveals the password.

---

### 🧪 Commands Used
- git clone ssh://bandit31-git@bandit.labs.overthewire.org:2220/home/bandit31-git/repo  
- cd repo  
- cat README.md  
- echo "May I come in?" > key.txt  
- git add key.txt  
- git commit -m "Add key.txt file"  
- git push origin master  

---

### 📸 Screenshots

**Creating the Required File and Preparing the Commit**

![Bandit Level 31 – File Creation](screenshots/level31_1.png)

---

**Pushing the Commit to the Remote Server to Receive the Password**

![Bandit Level 31 – Push Result](screenshots/level31_2.png)

---

### 🔑 Next Level Password
309RfhaqALVBEZpVb6LYStshZoqoSx5K

---

### 🧠 Explanation
The `git clone` command downloads the private repository for bandit31.  
The `cat README.md` command shows the instructions for the required file.  
The `echo` command creates a file named `key.txt` with the required content.  
The `git add` command stages the file for commit.  
The `git commit` command records the change in the local Git repository.  
The `git push` command sends the commit to the remote server, which validates the submission and returns the password.

---

### 🔐 Concept Learned
This level demonstrates how Git repositories can enforce workflows through remote validation.  
It shows how pushing commits to a remote repository can trigger server-side actions, a common mechanism used in CI/CD pipelines and security validation systems.
