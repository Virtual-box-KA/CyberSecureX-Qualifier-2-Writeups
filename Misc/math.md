# Math

> I was trying to implement RSA encryption again. I learnt my lesson from last time, so I'm not just using simple numbers... Can you help me recover the message? Here's what I used: n = 12407072677633161347 e = 65537 c = 6680131599371095691
>

# Step 1: RSA Decryption
Using RSA calculator we decoded these numbers into plain text integer values.

<img width="862" height="492" alt="image" src="https://github.com/user-attachments/assets/74bdb059-d57c-4c32-83be-9521397cade6" /><br>
M = 727361

# Step 2: The Trick
Now, we don’t convert m directly to hex bytes. Instead, we split them into
pairs of digits. <br>
72 73 61 <br>
Now, treat them as hex byte and convert them into text.

<img width="887" height="211" alt="image" src="https://github.com/user-attachments/assets/decf2c17-51dd-4490-b990-47df4f089781" />

So, the final flag is:<br>
```bash
FLAG{rsa}
```
