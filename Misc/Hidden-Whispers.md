# Hidden Whispers

A zip file *wall.jpg.gz* is given, extract it.\
We got a image, Visually its just a wall, Nothing unsual.

Let us check for any stegno, using 

```bash
steghide info wall.jpg
```

Okay there is something fishy asking for password 😄. Got some clue.
Just bruteforce the password, using command

```bash
stegcrack wall.jpg /usr/share/wordlists/rockyou.txt
```
This will crack the password.\

<img width="798" height="292" alt="image" src="https://github.com/user-attachments/assets/3952fd6e-ccf7-4db6-bdc1-7a25653264b7" />\

Here stegcrack gave us a file as well. Open it.

Yeahhhhhh!. The final flag is

```bash
flag{E4SY_ST3G_UNL0CK3D}
```
