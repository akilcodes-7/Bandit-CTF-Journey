## Bandit Level 28 → Level 29

### 🎯 Objective
Log in to the Bandit game as bandit28 and obtain the password for the next level by analyzing a Git repository where the credentials were previously removed.

---

### 🔑 Credentials Provided
Username: bandit28-git  
Password: Obtained from previous level  

---

### 🔍 Method of Solve
The password for the next level was removed from the current version of the repository, but it still exists in the Git commit history. By examining earlier commits, the original password can be recovered.

---

### 🧪 Commands Used
- git clone ssh://bandit28-git@bandit.labs.overthewire.org:2220/home/bandit28-git/repo  
- cd repo  
- cat README.md  
- git log -p  

---

### 📸 Screenshots

![Bandit Level 28 – Repository](screenshots/level28_1.png)

---

![Bandit Level 28 – Commit History](screenshots/level28_2.png)

---

### 🔑 Next Level Password
4pT1t5DENaYuqnqvadYs1oE4QLCdjmJ7

---

### 🧠 Explanation
The `git clone` command connects to the remote Git server over SSH and downloads the private repository.  
The `cd repo` command moves into the cloned repository directory.  
The `cat README.md` command displays the current version of the README file, which has the password removed.  
The `git log -p` command shows the complete commit history along with file differences. By examining earlier commits, the original README file containing the password is recovered.

---

### 🔐 Concept Learned
This level demonstrates that deleting sensitive data from a Git repository does not remove it from history.  
It highlights the importance of reviewing commit history when investigating data leaks and the need for proper secret-handling in version-controlled projects.
