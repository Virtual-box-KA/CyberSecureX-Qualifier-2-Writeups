
# Plug and Play

> A shady driver has been “plugged” into the system, but it’s definitely not playing nice. Rumor is, its IOCTL handler leaks secrets if you poke it the right way.

Given: A `.ova` file

Since it says `driver`, I uploaded the `.ova` file to Autopsy.

The file system was similar to Windows 2000, which the name also suggests.

<img width="1364" height="309" alt="image" src="https://github.com/user-attachments/assets/8b8dbd6a-a802-4785-8913-de22a76cca6a" />

I navigated to the Drivers folder located at:  
```bash
C:\Winit\System32\Drivers
````

<img width="462" height="164" alt="image" src="https://github.com/user-attachments/assets/3196ab0a-ffc1-47f8-8270-25ae5a41274f" />

After analyzing a bit, I found an unusual driver named **leakydrv.sys**

<img width="723" height="382" alt="image" src="https://github.com/user-attachments/assets/2d886759-cc39-48e6-a3be-e3c1af2e9d0d" />

I exported it and saved it to my device for further analysis.

<img width="118" height="123" alt="image" src="https://github.com/user-attachments/assets/11eb482d-d96d-4b2e-85a2-f2656a9d6ed3" />


