## Bandit Level 09 → Level 10

### 🎯 Objective
Log in to the Bandit game as bandit9 and obtain the password for the next level from a file by locating a readable string that contains repeated equals signs.

### 🔑 Credentials Provided
Username: bandit9  
Password: Obtained from previous level  

### 🔍 Method of Solve
The password for the next level is hidden inside a file named `data.txt`. The file contains many non-readable characters, but the password appears as a readable string that includes multiple `=` characters. Filtering readable strings helps identify it.

### 🧪 Commands Used
- strings data.txt | grep -e "="

![Bandit Level 09 Screenshot](screenshots/level09.png)

### 🔑 Next Level Password
FGUW5ilLVJrxX9kMYMntL4NgbpfMiqey

### 🧠 Explanation
The `strings data.txt` command extracts all human-readable strings from the file.  
The output is piped to `grep -e "="` to filter lines that contain repeated equals signs.  
Among the results, the line that clearly stands out contains the password required to proceed to the next level.

### 🔐 Concept Learned
This level demonstrates how to extract meaningful information from files containing mixed or binary data.  
It highlights pattern-based filtering using `grep` together with `strings` to efficiently locate hidden credentials.
