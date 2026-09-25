TryHackMe - The Game
My Introduction to HxD Hex Editor
The Challenge

The room gave the following prompt:

"Cipher has gone dark, but intel reveals he's hiding critical secrets inside Tetris, a popular video game. Hack it and uncover the encrypted data buried in its code."

The part that stood out to me was:

"encrypted data buried in its code"

My first thought was that if the flag was buried inside the game, then maybe I needed a way to look directly inside the file itself.

What I Did

I downloaded HxD and opened the file provided by the room:
tetrix.exe
Once the file was open, I used:
Ctrl + F
and searched for:
THM
I searched for THM because the answer input was xx{xx_xxx_xxxx_xx_xxx} so I knew it was a THM{..} typical flag.
After searching through the file, I found a readable text string containing the flag and completed the room.

What I Learned

Honestly, when I started this room I didn't really know what a hex editor was.

What I learned is that a hex editor lets you look at the actual contents of a file.

I understand now that files are made up of bytes, and the hex editor is simply showing those bytes in hexadecimal format.

I also learned that some files contain readable text hidden inside them.

like:

Flags
Passwords
URLs
Error messages
Usernames
Configuration information

without those things being visible when you normally open or run the file.

Hex Editor Basics

While learning about HxD, I found out that it shows three important things:

Offset - The location of the bytes in the file.

Hex Values - The raw bytes stored in the file shown in hexadecimal.

Text - A readable interpretation of those bytes when they represent characters.

Useful File Signatures (Magic Bytes)

Something I came across while learning about hex editors was that many file types have unique byte patterns at the beginning of the file.

These can be used to identify what a file really is.

PNG = 89 50 4E 47

ZIP = 50 4B 03 04

PDF = 25 50 44 46

Windows Executable (.exe) = 4D 5A

GIF = 47 49 46 38

JPEG = FF D8 FF

These are commonly called magic bytes or file signatures.

Takeaway

This room was my first real exposure to hex editors.
After completing the room, I understand that files are just a collection of bytes and that tools like HxD let you inspect those bytes directly. In this case, searching for the known TryHackMe flag prefix (THM) was enough to find the flag hidden inside the executable.
Happy Hunting :)
