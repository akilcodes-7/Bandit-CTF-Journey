## Bandit Level 03 → Level 04

### 🎯 Objective
Log in to the Bandit game as bandit3 and obtain the password for the next level from a hidden file inside a directory.

### 🔑 Credentials Provided
Username: bandit3  
Password: Obtained from previous level  

### 🔍 Method of Solve
The password for the next level is stored inside a hidden file located in a directory named `inhere`. To view hidden files, a detailed listing command must be used.

### 🧪 Commands Used
- ls  
- cd inhere  
- ls -alph  
- cat ...Hiding-From-You  

![Bandit Level 03 Screenshot](screenshots/level03.png)

### 🔑 Next Level Password
2WmrDFRmJIq3IPxneAaMGhap0pFhS3NJ

### 🧠 Explanation
The `ls` command lists the directory named `inhere`.  
The `cd inhere` command is used to move into the directory.  
The `ls -alph` command displays all files, including hidden ones, with detailed information.  
The file `...Hiding-From-You` is a hidden file, and its contents are displayed using the `cat` command to obtain the password.

### 🔐 Concept Learned
This level demonstrates how hidden files are handled in Linux.  
It highlights the importance of using appropriate command options to reveal hidden files and retrieve sensitive information.
