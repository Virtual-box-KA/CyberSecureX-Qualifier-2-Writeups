
# Echoes in the Deep

Given a zip file *deep_secrets.zip*,  
let us extract it.

Hmm, but it doesn't feel like a zip.  
We need to find out the file type:

```bash
file deep_secrets.zip
````

<img width="677" height="35" alt="image" src="https://github.com/user-attachments/assets/f419895b-6908-47de-b550-d6e8da467f00" />

Nice! We need to change the extension.
Use the command:

```bash
mv deep_secrets.zip deep_secrets.wav
```

Now let us try opening this file in tools like Audacity or Sonic Visualizer. Use any one of them. I used Sonic Visualizer.

Open this file:

<img width="1043" height="541" alt="image" src="https://github.com/user-attachments/assets/4dc5381a-dfbb-47d2-9677-a370fbc7520a" />

Oh, okay it feels like Morse again.

We can see:

1. Small length high pitch sounds - dots
2. Long length high pitch sounds - dashes
3. No pitch - spaces

Just convert that into strings.
The final flag is:

```bash
flag{s1gn4ls_fr0m_th3_d33p}
```

