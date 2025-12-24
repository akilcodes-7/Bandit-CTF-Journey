## Bandit Level 11 → Level 12

### 🎯 Objective
Log in to the Bandit game as bandit11 and obtain the password for the next level by decoding a text that is encrypted using a simple letter rotation.

### 🔑 Credentials Provided
Username: bandit11  
Password: Obtained from previous level  

### 🔍 Method of Solve
The password for the next level is stored in a file named `data.txt` that is encoded using ROT13. By applying a character translation, the original text can be revealed.

### 🧪 Commands Used
- ls -alph  
- cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'  

![Bandit Level 11 Screenshot](screenshots/level11.png)

### 🔑 Next Level Password
7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4

### 🧠 Explanation
The `ls -alph` command lists the files in the directory and shows the file `data.txt`.  
The `cat data.txt` command reads the encoded contents of the file.  
The output is piped to `tr 'A-Za-z' 'N-ZA-Mn-za-m'`, which performs a ROT13 transformation, converting each letter to its decoded form.  
The decoded output reveals the password for the next level.

### 🔐 Concept Learned
This level demonstrates how simple substitution ciphers such as ROT13 can be decoded using standard Linux tools.  
It highlights the usefulness of text processing utilities like `tr` for decrypting or transforming encoded data.
