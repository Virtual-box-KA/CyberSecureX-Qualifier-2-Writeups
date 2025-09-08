# EZ
Category - Reverse engineering <br>
Difficulty - Easy <br>
Points 150 <br>
Content = The app is engineered. All you have to do is go backwards.

# Using the file command
file rev1
# OUTPUT
rev1: ELF 64-bit LSB pie executable, x86-64, version 1 (SYSV), dynamically linked, interpreter /lib64/ld-linux-x86-64.so.2, BuildID[sha1]=255d897838bdcc2288ea7a22b3f7834a44eaf009, for GNU/Linux 4.4.0, stripped
#tried basic commands eg. strings objdump
#Using ghidra search the logic

Using Ghidra, I loaded the binary and explored the function list. The main functions of interest were:
- FUN_001097e0: final flag verification
- FUN_00108d80: checksum calculation
- FUN_00109470: input processing

<img width="1909" height="535" alt="sol" src="https://github.com/user-attachments/assets/d0d3aaeb-fe01-4ec5-8ebf-889f3616cc0c" />
<img width="1917" height="542" alt="sol1" src="https://github.com/user-attachments/assets/544cfcdc-d872-4bf0-a2e3-1ebe13e7804b" />
<img width="1906" height="549" alt="sol2" src="https://github.com/user-attachments/assets/056258f3-ed42-4812-b7f8-eca3bfcadc6e" />


# now we have found what we wanted 
Brute forcing string will take time but will be successful.
You can use GDB which is better.

# After doing all rhe analysis
nc 0.cloud.chals.io 11466
Enter password: LaCpadRNNbWr99
```bash
Correct! Flag is: flag{s0lvem3_pl5}
```




