## Bandit Level 04 → Level 05

### 🎯 Objective
Log in to the Bandit game as bandit4 and obtain the password for the next level from a file inside a directory that contains multiple files of different types.

### 🔑 Credentials Provided
Username: bandit4  
Password: Obtained from previous level  

### 🔍 Method of Solve
The password for the next level is stored inside one file that contains readable ASCII text. Other files contain binary or non-readable data. File type identification is required to locate the correct file.

### 🧪 Commands Used
- ls  
- cd inhere  
- ls -alph  
- find . -type f | xargs file  
- cat ./-file07  

![Bandit Level 04 Screenshot](screenshots/level04.png)

### 🔑 Next Level Password
koReBOKuIDDepwhWk7jZC0RTdopnAYKh

### 🧠 Explanation
The `ls` command lists the directory named `inhere`.  
The `cd inhere` command navigates into the directory.  
The `ls -alph` command displays all files with detailed information.  
The `find . -type f | xargs file` command identifies the type of each file.  
Only one file is identified as ASCII text.  
The `cat ./-file07` command is used to read that file and retrieve the password.

### 🔐 Concept Learned
This level demonstrates how to identify readable files among multiple files using file type analysis.  
It highlights the use of Linux pipelines and command chaining to efficiently locate meaningful data during enumeration.
