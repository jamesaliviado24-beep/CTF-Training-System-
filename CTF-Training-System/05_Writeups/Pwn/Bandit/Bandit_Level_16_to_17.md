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
