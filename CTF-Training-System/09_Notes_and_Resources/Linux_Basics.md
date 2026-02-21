# Linux Basics for CTF

## SSH
Connect to remote machine:
ssh username@host -p port

## ls
List files

ls -la → show hidden files

## cd
Change directory

## cat
Display file content

## file
Check file type

## find
Search files

Examples:
find . -size 1033c
find / -user bandit7 -size 33c

## grep
Search inside file

grep "text" filename

## sort
Sort lines

## uniq
Remove duplicate lines
uniq -u → show unique lines only

## strings
Extract readable strings from binary

## base64
Decode base64
base64 -d filename

## Pipe |
Send output to another command

Example:
sort data.txt | uniq -u
