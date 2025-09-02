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

