## Bandit Level 05 → Level 06

### 🎯 Objective
Log in to the Bandit game as bandit5 and obtain the password for the next level from a file that meets specific size and permission conditions.

### 🔑 Credentials Provided
Username: bandit5  
Password: Obtained from previous level  

### 🔍 Method of Solve
The password for the next level is stored inside a file that is human-readable, exactly 1033 bytes in size, and not executable. The file is located somewhere inside the `inhere` directory structure.

### 🧪 Commands Used
- ls -alph  
- cd inhere  
- ls -alph  
- find . -type f -size 1033c ! -executable  
- cat ./maybehere07/.file2  

![Bandit Level 05 Screenshot](screenshots/level05.png)

### 🔑 Next Level Password
HWasnPhtq9AVKe0dmk5nx2oC6U6aBG

### 🧠 Explanation
The `ls -alph` command is used to view directory contents with permissions and hidden files.  
The `cd inhere` command navigates into the target directory.  
The `find . -type f -size 1033c ! -executable` command searches for regular files that are exactly 1033 bytes in size and not executable.  
Only one file matches these conditions.  
The `cat ./maybehere07/.file2` command reads the contents of that file and reveals the password.

### 🔐 Concept Learned
This level demonstrates advanced file searching in Linux using size and permission filters.  
It highlights how combining multiple conditions with the `find` command helps efficiently locate sensitive information in large directory structures.
