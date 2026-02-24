# 🛡️ OverTheWire Bandit Writeup (Level 0–10)

Platform: OverTheWire Bandit  
Focus: Linux Fundamentals for Binary Exploitation  
Status: Completed  

---

# Level 0 → Level 1

## Goal
Login using SSH and find password inside file named readme.

## Commands Used
ssh
ls
cat

## Steps
ssh bandit0@bandit.labs.overthewire.org -p 2220
ls
cat readme

## What I Learned
- How to connect using SSH
- How to list files
- How to read file contents

---

# Level 1 → Level 2

## Goal
Password stored in file named "-"

## Problem
"-" is treated as an option.

## Solution
cat ./-

## What I Learned
- Use ./ before special filenames

---

# Level 2 → Level 3

## Goal
Password stored in file with spaces in name.

## Solution
cat "--spaces in this filename--"

OR

cat -- --spaces\ in\ this\ filename--

## What I Learned
- Use quotes for filenames with spaces
- Escape spaces with \

---

# Level 3 → Level 4

## Goal
Password stored in hidden file inside "inhere"

## Solution
ls
cd inhere
ls -la
cat .hiddenfilename

## What I Learned
- Hidden files start with .
- Use ls -la to see hidden files

---

# Level 4 → Level 5

## Goal
Password is in the only human-readable file.

## Solution
cd inhere
file *
cat filename

## What I Learned
- file command checks file type

---

# Level 5 → Level 6

## Goal
File must be:
- human-readable
- 1033 bytes
- not executable

## Solution
find . -type f -size 1033c ! -executable
cat filepath

## What I Learned
- find can filter by size
- ! means NOT
- combine multiple conditions

---

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

---

# Level 7 → Level 8

## Goal
Password next to word "millionth"

## Solution
grep "millionth" data.txt

## What I Learned
- grep searches inside files

---

# Level 8 → Level 9

## Goal
Find the only unique line.

## Solution
sort data.txt | uniq -u

## What I Learned
- sort + uniq combination
- Command piping |

---

# Level 9 → Level 10

## Goal
Password in readable strings preceded by ===

## Solution
strings data.txt | grep "==="

## What I Learned
- strings extracts readable text from binary files

---

# Level 10 → Level 11

## Goal
File contains base64 encoded data.

## Solution
base64 -d data.txt

## What I Learned
- Base64 decoding
- Encoded data in challenges

---

# Overall Skills Built

- SSH usage
- File navigation
- Handling special filenames
- Hidden files
- File type checking
- Searching by size
- Searching by owner
- Text searching with grep
- Command chaining
- Base64 decoding

These are foundations for binary exploitation.
