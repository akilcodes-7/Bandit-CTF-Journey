## Bandit Level 00 → Level 01

### 🎯 Objective
Log in to the Bandit game using the given credentials and obtain the password for the next level by reading the readme file.

### 🔑 Credentials Provided
Username: bandit0  
Password: bandit0  

### 🔍 Method of Solve
The password for the next level is stored inside a file named readme in the home directory. By listing the files and reading the contents of the file, the password can be obtained.

### 🧪 Commands Used
- ls  
- cat readme

![Bandit Level 00 Screenshot](screenshots/level00.png)

### 🔑 Next Level Password
ZjlJTmM6FvvyRnrB2rfNWOZOTa6ip5If

### 🧠 Explanation
The ls command is used to list the files present in the current directory.  
The cat readme command displays the contents of the readme file.  
The output of the file reveals the password required to log in to the next Bandit level.

### 🔐 Concept Learned
This level introduces basic Linux command-line usage.  
It demonstrates how files can be accessed and how sensitive information such as passwords may be stored inside files in a Linux system.
