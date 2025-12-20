## Bandit Level 08 → Level 09

### 🎯 Objective
Log in to the Bandit game as bandit8 and obtain the password for the next level from a file by identifying the unique line.

### 🔑 Credentials Provided
Username: bandit8  
Password: Obtained from previous level  

### 🔍 Method of Solve
The password for the next level is stored inside a file named `data.txt`. The file contains many repeated lines, and the required password is the line that appears only once. Sorting and counting duplicate lines helps identify the unique entry.

### 🧪 Commands Used
- ls -alph  
- sort data.txt | uniq -c  

![Bandit Level 08 Screenshot](screenshots/level08.png)

### 🔑 Next Level Password
4CKMh1JI91pXZ2P0gaGan4xvgAdJm

### 🧠 Explanation
The `ls -alph` command lists all files in the directory, showing the presence of `data.txt`.  
The `sort data.txt` command sorts all lines alphabetically.  
The output is piped to `uniq -c`, which counts how many times each line appears.  
The line with a count of `1` is the unique line and contains the password for the next level.

### 🔐 Concept Learned
This level demonstrates how to analyze repeated data using sorting and filtering techniques.  
It highlights the effective use of command pipelines and text-processing utilities such as `sort` and `uniq` to extract meaningful information.
