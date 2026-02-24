# Level 6 → Level 7

## Goal
File must be:
- owned by bandit7
- group bandit6
- 33 bytes

## Solution
find / -type f -user bandit7 -group bandit6 -size 33c 2>/dev/null
cat filepath

## What I Learned
- Search entire system
- 2>/dev/null hides permission errors
