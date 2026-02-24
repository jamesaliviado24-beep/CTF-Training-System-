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
