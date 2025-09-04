
# Hidden Whispers

> Sometimes secrets aren’t locked too tightly — you just need the right word to open the door.

A zip file *wall.jpg.gz* is given, extract it.  
We got an image; visually, it's just a wall, nothing unusual.

Let us check for any stegno using:

```bash
steghide info wall.jpg
````

Okay, there is something fishy, it's asking for a password 😄. Got some clue from steghide.
Just brute force the password using the command:

```bash
stegcrack wall.jpg /usr/share/wordlists/rockyou.txt
```

This will crack the password.

<img width="798" height="292" alt="image" src="https://github.com/user-attachments/assets/3952fd6e-ccf7-4db6-bdc1-7a25653264b7" />

Here, stegcrack gave us a file as well. Open it.

Yeahhhhhh! The final flag is:

```bash
flag{E4SY_ST3G_UNL0CK3D}
```
