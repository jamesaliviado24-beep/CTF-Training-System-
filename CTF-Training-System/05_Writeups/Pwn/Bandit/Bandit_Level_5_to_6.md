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
