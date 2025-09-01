# Capture 1

We have been given a pcap file, Let us just check if there is any direct flag written in it

Let us use 
```bash 
strings  file.pcapng
```

There is something that makes me happy, The FLAAAAG!








 ```bash
**flag{h3r3_7t_i5}**
```

My Hates to the OC, it was a decoy

But let us see if there is something else - 
Agh it just says gebberish, 
But hey! I see something unusal, **dot, dash**
Probaby Morse Code??

Let us try !!!!
First find all the packet is squence, open the file in wireshark, add filter *frame contains dot*
i got the protocol, That's ICMP

Treverse through the all the packets the protocol
Write those dots and dashes 

Decode from the morse-
FINALLLYYYYYYY!

Here is the flag - 
```bash
**flag{t3l3gr4m_ftw}**
```

