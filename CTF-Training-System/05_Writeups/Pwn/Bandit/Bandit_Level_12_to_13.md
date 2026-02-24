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
