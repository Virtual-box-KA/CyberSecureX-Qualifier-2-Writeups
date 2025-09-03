# Plug and Play

> A shady driver has been “plugged” into the system, but it’s definitely not playing nice. Rumor is, its IOCTL handler leaks secrets if you poke it the right way.

Given - A `.ova` file

It says `driver`, so I uploaded the ova file to autopsy. 

The file system was similar to win2000, also the name suggests.

<img width="1364" height="309" alt="image" src="https://github.com/user-attachments/assets/8b8dbd6a-a802-4785-8913-de22a76cca6a" /> <br>

I Navigated to the Drivers folder loacated at, 
```bash
C:\Winit\System32\Drivers
```
<img width="462" height="164" alt="image" src="https://github.com/user-attachments/assets/3196ab0a-ffc1-47f8-8270-25ae5a41274f" /><br>

After analyzing a bit, I found a unusual driver named **leakydrv.sys**

<img width="723" height="382" alt="image" src="https://github.com/user-attachments/assets/2d886759-cc39-48e6-a3be-e3c1af2e9d0d" /><br>

I hit export and saved to my device for further analysis.

<img width="118" height="123" alt="image" src="https://github.com/user-attachments/assets/11eb482d-d96d-4b2e-85a2-f2656a9d6ed3" />
