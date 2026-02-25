# OverTheWire Bandit Writeup (Level 11–20)

---

# Level 11 → Level 12

## Goal
The file `data.txt` contains text where all letters have been rotated by 13 positions (ROT13). Retrieve the real password.

## Concept
ROT13 shifts letters 13 places in the alphabet.

## Solution
Use `tr` to rotate letters back:

tr 'A-Za-z' 'N-ZA-Mn-za-m' < data.txt

## What I Learned
- ROT13 is a simple substitution cipher
- `tr` can transform characters
- Basic encoding/decoding techniques

---

# Level 12 → Level 13

## Goal
`data.txt` is a hexdump of a repeatedly compressed file.

## Concept
- Convert hexdump back to binary
- Identify compression type
- Extract repeatedly

## Steps

1. Create working directory:
mktemp -d

2. Copy file:
cp data.txt /tmp/yourdir

3. Convert from hex:
xxd -r data.txt > file

4. Identify file type:
file file

5. If compressed:
- gzip → gunzip
- bzip2 → bunzip2
- tar → tar -xvf

Repeat until readable text appears.

## What I Learned
- Using /tmp safely
- `xxd -r` reverses hexdump
- `file` identifies file type
- Compression layers can stack

---

# Level 13 → Level 14

## Goal
Use provided private SSH key to log into next level.

## Concept
SSH authentication using private key.

## Steps

1. Save private key to a file:
nano keyfile

2. Set proper permissions:
chmod 600 keyfile

3. Login using key:
ssh -i keyfile bandit14@localhost -p 2220

4. Read password:
cat /etc/bandit_pass/bandit14

## What I Learned
- SSH key authentication
- Importance of file permissions (600)
- Private key security

---

# Level 14 → Level 15

## Goal
Submit current password to port 30000 on localhost.

## Concept
Communicating with a local service using netcat.

## Solution
echo "current_password" | nc localhost 30000

## What I Learned
- Using netcat to connect to services
- Client-server communication basics

---

# Level 15 → Level 16

## Goal
Submit password to port 30001 using SSL/TLS.

## Concept
Encrypted connection required.

## Solution
openssl s_client -connect localhost:30001

Then paste password when prompted.

## What I Learned
- Difference between plain TCP and SSL
- Using openssl s_client
- Basic TLS understanding

---

# Level 16 → Level 17

## Goal
Find correct port between 31000–32000 that returns credentials.

## Concept
Port scanning + identifying SSL service.

## Steps
1. Scan all ports in range
nmap -p 31000-32000 localhost

2. Identify open ports from scan results
# Example: 31046, 31518, 31691, 31790, 31960

3. Test each open port for SSL
openssl s_client -connect localhost:PORT

4. Submit current Bandit16 password on correct SSL port
Server returns SSH private key for Bandit17

5. Save the key locally
nano ~/bandit17.key
# Paste full RSA private key
chmod 600 ~/bandit17.key

6. SSH into Bandit17 using the key
ssh -i ~/bandit17.key bandit17@bandit.labs.overthewire.org -p 2220

## What I Learned
- Basic port scanning
- Service enumeration
- Distinguishing SSL vs non-SSL services

---

# Level 17 → Level 18

## Goal
Find difference between passwords.old and passwords.new.

## Solution
diff passwords.old passwords.new

The changed line is the password.

## What I Learned
- Using `diff`
- Comparing file versions
- Identifying modified lines

---

# Level 18 → Level 19

## Goal
.bashrc logs you out immediately after SSH login.

## Concept
Bypass shell execution.

## Solution
ssh bandit18@bandit.labs.overthewire.org -p 2220 cat readme

This executes `cat readme` without starting interactive shell.

## What I Learned
- SSH can run commands directly
- Shell initialization files can be bypassed

---

# Level 19 → Level 20

## Goal
Use setuid binary in home directory.

## Concept
SetUID allows a program to run with file owner's privileges.

## Steps

1. Execute binary:
./bandit20-do

2. Follow usage instructions:
./bandit20-do cat /etc/bandit_pass/bandit20

## What I Learned
- What SetUID is
- How privilege escalation works
- Running commands with elevated privileges

---

# Skills Built (Levels 11–20)

- ROT13 decoding
- Hexdump reversal
- Multi-layer compression extraction
- SSH key authentication
- Netcat usage
- SSL/TLS connections
- Port scanning
- File comparison
- Shell bypass techniques
- SetUID privilege concepts

These levels introduce networking, encryption, and privilege concepts — foundations for real penetration testing.
