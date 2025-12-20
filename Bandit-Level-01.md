## Bandit Level 01 → Level 02

### 🎯 Objective
Log in to the Bandit game as bandit1 and obtain the password for the next level from a file named `-`.

### 🔑 Credentials Provided
Username: bandit1  
Password: Obtained from previous level  

### 🔍 Method of Solve
The password for the next level is stored in a file named `-`. Since files starting with a hyphen are treated as command options, the file must be accessed using a relative path to avoid misinterpretation.

### 🧪 Commands Used
- ls  
- cat ./-  

![Bandit Level 01 Screenshot](screenshots/level01.png)

### 🔑 Next Level Password
263JGJPfgU6LtdEvfgWU1XP5yac29mFx

### 🧠 Explanation
The `ls` command is used to list the files present in the directory and reveals a file named `-`.  
The `cat ./-` command explicitly tells the shell to treat `-` as a file in the current directory instead of an option.  
This allows the contents of the file to be read successfully.

### 🔐 Concept Learned
This level demonstrates how Linux interprets filenames that start with special characters.  
It highlights the importance of using relative paths to safely access files during enumeration.
