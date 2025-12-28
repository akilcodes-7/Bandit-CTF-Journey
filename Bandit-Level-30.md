## Bandit Level 30 → Level 31

### 🎯 Objective
Log in to the Bandit game as bandit30 and obtain the password for the next level by inspecting Git tags inside a private repository.

---

### 🔑 Credentials Provided
Username: bandit30-git  
Password: Obtained from previous level  

---

### 🔍 Method of Solve
The password is not stored in the main files of the repository. Instead, it is hidden inside a Git tag. By listing available tags and viewing the data stored inside the tag, the password can be recovered.

---

### 🧪 Commands Used
- git clone ssh://bandit30-git@bandit.labs.overthewire.org:2220/home/bandit30-git/repo  
- cd repo  
- cat README.md  
- git tag  
- git show-ref --tags  
- git show secret  

---

### 📸 Screenshots

**Cloning the Repository and Checking Files**

![Bandit Level 30 – Repository](screenshots/level30_1.png)

---

**Viewing the Hidden Git Tag That Contains the Password**

![Bandit Level 30 – Git Tag](screenshots/level30_2.png)

---

### 🔑 Next Level Password
fb552xb7bRyFmAvQYQEGqsbhVyJqhnDy

---

### 🧠 Explanation
The `git clone` command downloads the private repository over SSH.  
The `cat README.md` command shows that the file does not contain the password.  
The `git tag` command lists all Git tags in the repository, revealing a tag named `secret`.  
The `git show-ref --tags` command confirms the internal reference of the tag.  
The `git show secret` command displays the content stored inside the tag, which contains the password.

---

### 🔐 Concept Learned
This level demonstrates how Git tags can store important information.  
It highlights that sensitive data may exist in tags even when it is not visible in files or branches, emphasizing the need to inspect all Git references during security investigations.
