## Bandit Level 07 → Level 08

### 🎯 Objective
Log in to the Bandit game as bandit7 and obtain the password for the next level from a file by identifying a specific readable string.

### 🔑 Credentials Provided
Username: bandit7  
Password: Obtained from previous level  

### 🔍 Method of Solve
The password for the next level is hidden inside a file named `data.txt`. The file contains many unreadable characters, but the required password appears as a readable string next to a specific keyword.

### 🧪 Commands Used
- ls -alph  
- strings data.txt | grep "millionth"  

![Bandit Level 07 Screenshot](screenshots/level07.png)

### 🔑 Next Level Password
dfwvzFQi4mU0wfNbFOe9R0WSkMlzGeEc

### 🧠 Explanation
The `ls -alph` command lists all files in the directory, revealing the file `data.txt`.  
The `strings data.txt` command extracts all human-readable strings from the file.  
The output is piped to `grep "millionth"` to search for the line containing the keyword `millionth`.  
The matching line contains the password required to proceed to the next level.

### 🔐 Concept Learned
This level demonstrates how to extract readable information from binary or mixed-content files.  
It highlights the use of command pipelines and text filtering tools such as `strings` and `grep` during enumeration.
