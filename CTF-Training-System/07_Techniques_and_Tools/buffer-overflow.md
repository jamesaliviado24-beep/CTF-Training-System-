# Buffer Overflow

A buffer overflow occurs when a program writes more data into a buffer than it can hold.

Example vulnerable code:

char buffer[32];
gets(buffer);

If the user enters more than 32 bytes, the extra data overwrites adjacent memory.

Testing method:

Send progressively longer input strings.

Example:

AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA

If the program crashes or behaves unexpectedly, a buffer overflow may exist.

Key concept:

Buffer → Saved registers → Return address

Overflowing the buffer may allow control over program execution.
