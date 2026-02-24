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
