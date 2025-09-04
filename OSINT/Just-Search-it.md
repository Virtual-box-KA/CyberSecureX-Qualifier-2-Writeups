# Just Search It  
Points: 200  
Category: OSINT

After analyzing the image, the idea came to my mind that it’s a conference image and the code behind it was an error message in Rust language.  
It was clear that it was a Rust conference. Moreover, the image has the short form *(con)* written on it.

I searched on Google for recent Rust conferences. Most were online, which were of no use.  
Then I tried to visually analyze the people sitting there — they seemed to have Asian looks.  
I searched for recent offline conferences in Asia and got many results: Singapore, Beijing, Japan.  
Finally, something clicked: **RUST CON ASIA 2019**.

<img width="1084" height="464" alt="image" src="https://github.com/user-attachments/assets/9e4bd347-6d11-49d0-ab71-f6d0e643d361" />

I searched it on YouTube to find its videos.  
Found a playlist, played the videos at 2x speed and skipped many parts.  
On **video no. 1** in the playlist, I got the exact frame given in the challenge, timestamped **15:02**.

<img width="864" height="533" alt="image" src="https://github.com/user-attachments/assets/a14384b2-61f6-48f2-ad1f-85c89434b090" />

In the description, I found a GitHub repo. Out of curiosity, I visited that repo.

<img width="821" height="379" alt="image" src="https://github.com/user-attachments/assets/c23ea38d-8623-46f5-b493-85b5d7225c43" />

Scrolled a bit and saw an open issue (now closed).  
There was the flag!

<img width="466" height="315" alt="image" src="https://github.com/user-attachments/assets/46c36189-8886-48f4-89a1-5840b084f92d" />

The final flag was:

```bash
flag{f0und_th3_s0urc3_l1k3_a_b0ss}
