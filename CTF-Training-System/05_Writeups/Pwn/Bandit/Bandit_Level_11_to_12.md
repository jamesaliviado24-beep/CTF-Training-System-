# Level 11 → Level 12

## Goal
The file `data.txt` contains text where all letters have been rotated by 13 positions (ROT13). Retrieve the real password.

## Concept
ROT13 shifts letters 13 places in the alphabet.

## Solution
Use `tr` to rotate letters back:

tr 'A-Za-z' 'N-ZA-Mn-za-m' < data.txt

## What I Learned
- ROT13 is a simple substitution cipher
- `tr` can transform characters
- Basic encoding/decoding techniques
