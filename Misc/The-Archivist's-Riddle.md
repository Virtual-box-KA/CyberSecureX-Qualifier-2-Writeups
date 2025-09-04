
## The Archivist's Riddle

> The enigmatic Archivist has left you a single file, a digital inheritance. He claims it holds the key to a truth long hidden, a secret buried within layers of logic and code. He told you, "To uncover the whole truth, you must not only look at the parts but also the sum of them." He also mumbled something about a "picture worth a thousand words." Look for what remains, what is often discarded — the essence that gives form to the formless.

Given a zip file: `challenge.zip`

---

The file doesn't seem like a zip file, so I used:

```bash
file challenge.zip
````

Bang on! It was a shell script. I just renamed it to `challenge.sh`.

Then I tried to find if there was any flag written in it directly using:

```bash
strings challenge.sh | grep -i flag
```

![image](https://github.com/user-attachments/assets/077cb2c5-e16e-4239-bd0a-f39e87caa75d)

Probably the first part and a hint for the flag, to look somewhere else. I contacted the organizers for the same.

They sent me the flag.

### The final flag:

```bash
flag{executing_the_truth}
```

