## Bandit Level 02 → Level 03

### 🎯 Objective
Log in to the Bandit game as bandit2 and obtain the password for the next level from a file that contains spaces in its filename.

### 🔑 Credentials Provided
Username: bandit2  
Password: Obtained from previous level  

### 🔍 Method of Solve
The password for the next level is stored in a file whose name contains spaces. Such filenames must be handled carefully so that the shell interprets the name correctly.

### 🧪 Commands Used
- ls  
- cat spaces\ in\ this\ filename  

![Bandit Level 02 Screenshot](screenshots/level02.png)

### 🔑 Next Level Password
MNk8KNH3Usi14PLUODpFqfxLP1Smx

### 🧠 Explanation
The `ls` command lists the files in the directory and shows a file with spaces in its name.  
The `cat spaces\ in\ this\ filename` command uses backslashes to escape the spaces, allowing the file to be read correctly.  
The output of the file reveals the password required to proceed to the next level.

### 🔐 Concept Learned
This level demonstrates how Linux handles filenames that contain spaces.  
It highlights the importance of escaping special characters when working with files in the command line.
