
# **Bandit Levels 1–20: Techniques and Tools**

## **Levels 1–10: Linux Basics**

**Techniques:**

* SSH login using username/password
* Navigating directories: `cd`, `ls`, `pwd`
* Viewing files: `cat`, `less`, `head`, `tail`
* Searching for files and content: `find`, `grep`
* Understanding file types: `file`
* File size info: `du`
* File permissions: `chmod` basics

**Tools:**

* Bash / Linux terminal
* `ssh`
* `ls`, `cd`, `cat`, `file`, `du`, `find`, `grep`

---

## **Levels 11–15: Encodings, Keys, and Local Connections**

**Techniques:**

* Decoding Base64: `base64 -d`
* ROT13 decoding: `tr 'A-Za-z' 'N-ZA-Mn-za-m'`
* Hex dump to binary conversion: `xxd -r file.hex > file`
* Creating temporary directories: `mkdir /tmp/tmpname`, `mktemp -d`
* Saving private keys: `echo "KEY" > file.key`
* Setting proper permissions: `chmod 600 file.key`, `chmod 700 script.sh`
* Using private SSH key to login: `ssh -i file.key user@host -p PORT`

**Tools:**

* `xxd`, `tr`, `base64`, `mkdir`, `mktemp`, `echo`, `chmod`, `ssh`

---

## **Levels 16–17: Port Scanning & SSL**

**Techniques:**

* Port scanning a range: `nmap -p 31000-32000 localhost`
* Identifying open ports
* Checking SSL/TLS ports: `openssl s_client -connect localhost:PORT`
* Submitting password to correct port
* Understanding differences between SSL and non-SSL ports

**Tools:**

* `nmap`
* `openssl s_client`
* `nc` / `netcat`
* Bash shell commands

---

## **Levels 18–20: Setuid, Diff, and Binary Execution**

**Techniques:**

* Comparing files for differences: `diff file1 file2`
* Using setuid binaries to get passwords
* Handling shell logout issues caused by `.bashrc`
* Submitting password to local service / binary execution

**Tools:**

* `diff`
* Local shell commands: `./binary`, `cat`, `ls`
* `ssh`

---
