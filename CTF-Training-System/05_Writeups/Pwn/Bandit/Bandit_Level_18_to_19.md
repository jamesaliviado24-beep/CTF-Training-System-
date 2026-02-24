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
