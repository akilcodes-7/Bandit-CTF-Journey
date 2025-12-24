## Bandit Level 12 → Level 13

### 🎯 Objective
Log in to the Bandit game as bandit12 and obtain the password for the next level by extracting data from a file that has been compressed and archived multiple times.

---

### 🔑 Credentials Provided
Username: bandit12  
Password: Obtained from previous level  

---

### 🔍 Method of Solve
The password for the next level is stored in a file that has been repeatedly compressed using multiple formats such as gzip, bzip2, and tar. The file must be decoded layer by layer until a readable text file is obtained.

---

### 🧪 Commands Used
- mkdir /tmp/ctf  
- cp data.txt /tmp/ctf  
- cd /tmp/ctf  
- xxd -r data.txt > data  
- file data  
- mv data data.gz  
- gzip -d data.gz  
- file data  
- mv data data.bz2  
- bzip2 -d data.bz2  
- file data  
- mv data data.tar  
- tar -xvf data.tar  
- file data5.bin  
- mv data5.bin a.tar  
- tar -xvf a.tar  
- file data6.bin  
- mv data6.bin ak.gz  
- gzip -d ak.gz  
- file ak  
- cat ak  

---

### 📸 Screenshots
![Bandit Level 12 – Part 1](screenshots/level12_1.png)  
![Bandit Level 12 – Part 2](screenshots/level12_2.png)

---

### 🔑 Next Level Password
FO5dwFsc0cbaIiH0h8J2eUks2vdTDwAn

---

### 🧠 Explanation
A temporary working directory was created using `mkdir /tmp/ctf` so extraction operations could be performed in a writable location.  
The file `data.txt` was copied into this directory using `cp` to avoid permission issues in the home directory.  
The `cd /tmp/ctf` command moved into the working directory where all extraction steps were executed.

The `xxd -r data.txt > data` command converted the hexadecimal representation back into its original binary form.  
The `file data` command identified the format of the decoded file so the correct extraction method could be chosen.

The file was renamed to `data.gz` and decompressed using `gzip -d data.gz`.  
The `file data` command was used again to determine the new file format.

The file was renamed to `data.bz2` and decompressed using `bzip2 -d data.bz2`.  
The `file data` command identified the next archive format.

The file was renamed to `data.tar` and extracted using `tar -xvf data.tar`.  
The `file data5.bin` command detected another archived file, which was renamed to `a.tar` and extracted using `tar -xvf a.tar`.

The file `data6.bin` was identified as gzip-compressed, so it was renamed to `ak.gz` and decompressed using `gzip -d ak.gz`.  
The `file ak` command confirmed the final file was plain ASCII text, and `cat ak` displayed its contents, revealing the password.

---

### 🔐 Concept Learned
This level demonstrates how multi-layered compression and encoding are used to hide information.  
It highlights the importance of file type identification and the use of multiple Linux extraction tools to recover hidden data during forensic analysis and CTF challenges.
