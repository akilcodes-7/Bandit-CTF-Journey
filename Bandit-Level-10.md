## Bandit Level 10 → Level 11

### 🎯 Objective
Log in to the Bandit game as bandit10 and obtain the password for the next level by decoding a Base64-encoded file.

### 🔑 Credentials Provided
Username: bandit10  
Password: Obtained from previous level  

### 🔍 Method of Solve
The password for the next level is stored in a file named `data.txt`, which is encoded using Base64. Decoding the file reveals the plaintext password.

### 🧪 Commands Used
- ls -alph  
- base64 -d data.txt  

![Bandit Level 10 Screenshot](screenshots/level10.png)

### 🔑 Next Level Password
dR173fZKbORRSDGSGgZRWnpNV3qRr

### 🧠 Explanation
The `ls -alph` command lists the files in the directory and shows the presence of `data.txt`.  
The `base64 -d data.txt` command decodes the Base64-encoded content of the file.  
The decoded output directly reveals the password required for the next level.

### 🔐 Concept Learned
This level demonstrates how encoded data can be decoded using standard Linux utilities.  
It highlights the importance of recognizing common encoding formats such as Base64 during enumeration and analysis.
