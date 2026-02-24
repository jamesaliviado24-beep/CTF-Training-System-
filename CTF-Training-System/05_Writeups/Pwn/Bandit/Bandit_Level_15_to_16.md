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
