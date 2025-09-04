## The Archivist's Riddle

>The enigmatic Archivist has left you a single file, a digital inheritance. He claims it holds the key to a truth long hidden, a secret buried within layers of logic and code. He told you, "To uncover the whole truth, you must not only look at the parts but also the sum of them." He also mumbled something about a "picture worth a thousand words." . Look for what remains, what is often discarded, the essence that gives form to the formless.

Given a zip file, `challenge.zip`

--- 
The file dosent seem like a zip file, So is ued 
```bash
file challenge.zip
```
Bang on, It was a shell script, I just renamed it to challenge .sh
Then i tried to find if there is any flag written in it directly used 
```bash
strings challenge.sh | grep -i flag
```

<img width="711" height="204" alt="image" src="https://github.com/user-attachments/assets/077cb2c5-e16e-4239-bd0a-f39e87caa75d" />

Got this, probably the first part and hint for the flag, to look somewhere else. I Contacted the organizers for the same.
The sent me the flag.

The final flag:
```bash
flag{executing_the_truth}
```
