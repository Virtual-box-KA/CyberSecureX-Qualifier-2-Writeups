# Just search it
Points 200 <br>
Category - OSINT

After analyzing the image, the idea came to my mind its a conference image and the code behind was the error in rust language.
It was final that it was a Rust conference, morever there its is written in the image in short form (con).

I searched on Google for recent rust conference, it showed conferences, most were in online mode which were of no use. I tried to visually analzse the people sitting there.
Seemed to be with Asian looks. Then I searched recent conferences, which took place offline in Asia, I got many, Singapore, Beijng, Japan.
Finally something clicked as `RUST CONASIA 2019`.

<img width="1084" height="464" alt="image" src="https://github.com/user-attachments/assets/9e4bd347-6d11-49d0-ab71-f6d0e643d361" />


I Searched it on youtubes to find its video.  Got a playlist, played the video in 2x, and skipped in many parts, on `video no 1` itself in the playlist, i got the exact frame given in the challenge, having timestamp `15:02`.

<img width="864" height="533" alt="image" src="https://github.com/user-attachments/assets/a14384b2-61f6-48f2-ad1f-85c89434b090" />

In the comments, i got a github repo. 

<img width="821" height="379" alt="image" src="https://github.com/user-attachments/assets/c23ea38d-8623-46f5-b493-85b5d7225c43" /> <br>

Srolled a bit, saw an open issue (now closed), there was the flag !!

<img width="466" height="315" alt="image" src="https://github.com/user-attachments/assets/46c36189-8886-48f4-89a1-5840b084f92d" />

The final flag was - 
```bash
flag{f0und_th3_s0urc3_l1k3_a_b0ss}
```
