# Echoes in the Deep

Given a zip file *"deep_secrets.zip"*
let us extarct it

Hmm, but it doesn't feel like a zip
Need to find out the file type

```bash
file deep_secrets.zip
```

<img width="677" height="35" alt="image" src="https://github.com/user-attachments/assets/f419895b-6908-47de-b550-d6e8da467f00" />

Noice, we need to change the extension
Use command

```bash
mv deep_secrets.zip deep_secrets.wav
```

Now let us just try to open this file in tools like, Audacity or Sonic-Visualizer. Use any
i used sonic visualizer


Open this file

<img width="1043" height="541" alt="image" src="https://github.com/user-attachments/assets/4dc5381a-dfbb-47d2-9677-a370fbc7520a" />


Ohh okay, Feels like morse again. 

We can see some, 
1. small length high pitch sounds - dots
2. Long length high pitch sounds - dashes
3. And no pitches - spaces

Just convert that into strings
The final flag is 
```bash
flag{s1gn4ls_fr0m_th3_d33p}
```
