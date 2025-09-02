# Web-access.md
**Points - 250**

Given - A zip file, web_access

Let us try to extract it, 
It asks for password. Let us try to bruteforce if

Using 
```bash
zip2john web_access > hash.txt
john hash.txt --wordlist=/usr/share/wordlists/rockyou.txt
```

Okay, it Took a day but coundnt bruteforce it

Later comes the hint 

<img width="378" height="79" alt="image" src="https://github.com/user-attachments/assets/83c62a3f-5834-4270-8da6-5d37addd4fcb" />

The sentence that comes to my mind
> thequickbrownfoxjumpsoverthelazydog

Yeaaaah ! That's the password, Got another file. 
Seems a log file

