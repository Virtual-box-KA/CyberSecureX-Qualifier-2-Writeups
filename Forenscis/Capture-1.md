# Capture 1
> The 3 little pigs are the best of friends. But 1 little pig suspects that 2 little pigs maybe scheming behind his back. The 2 little pigs know how to hide messages in network but (fortunately for you) not well enough.
 
We have been given a pcap file, Let us just check if there is any flag directly written in it

Let us use 
```bash 
strings  file.pcapng
```

There is something that makes me happy, The FLAAAAG!

<img width="184" height="30" alt="image" src="https://github.com/user-attachments/assets/1f6f3e9c-3546-4ecd-b390-401638ce89c0" />

 ```bash
flag{h3r3_7t_i5}
```

> **My Hates to the OC, it was a decoy** 😠
---
But let us see if there is something else - 
Agh it just says gibberish, 
But hey! I see something unusal, **dot, dash**

<img width="687" height="325" alt="image" src="https://github.com/user-attachments/assets/ca67d73e-9850-41db-a535-a73166a1da8d" />

Probaby Morse Code??

Let us try !!!!
First find all the packet is squence, open the file in wireshark, add filter 

```bash
frame contains dot
```

i got the protocol, That's ICMP

Traverse through the all the packets the protocol
Write those dots and dashes 

Decode from the morse-
FINALLLYYYYYYY!

Here is the flag - 
```bash
flag{t3l3gr4m_ftw}
```

