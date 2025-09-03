📝 Writeup – Acme Corp Web Challenge

📌 Challenge Description

Acme Corp

Check out Acme Corp's old website.
URL: https://cybersecure-x-web-ez.chals.io/

We are tasked with exploring the migrated Acme Corp website to recover pieces of the flag hidden across legacy files. The flag is split into 5 parts, each embedded in different locations on the site.
________________________________________
🔎 Step 1: 
HTML Source Inspecting the page source (Ctrl+U or DevTools → Elements tab), we find a comment in the <head> section:        

<!-- build artifact:
 [1/5]-S3GM
 (note to self: admin panel moved, TODO remove robots entries)
-->

Part 1/5 = S3GM
________________________________________
🎨 Step 2: CSS File

Checking style.css (visible in DevTools → Network tab), near the bottom there’s a developer comment:
/* build note:
 [2/5]-3NT_
*/

Part 2/5 = 3NT_
________________________________________
⚙️ Step 3: JavaScript File
Opening app.js, there are some distractions (FLAGS array, reversed strings), but the real clue is in the scratchpad comment:

/*
   build scratchpad:
   The release engineer left fragments here but reversed to be "compact":
   ]'3/5[' = ]'3R0F'[    // reversed
*/

Reversing '3R0F' gives us:

Part 3/5 = F0R3
________________________________________
🤖 Step 4: robots.txt
Navigating to /robots.txt, we see:
User-agent: *
Disallow: /admin
Disallow: /admin-old
Disallow: /private

audit note:
[4/5]-NS1C

Part 4/5 = NS1C
________________________________________
🕵️ Step 5: Hidden File Discovery

The description hinted at Acme’s “old website” and “legacy stuff”. Using ffuf (forced browsing), we brute-forced hidden files:
ffuf -u https://cybersecure-x-web-ez.chals.io/FUZZ -w /usr/share/wordlists/seclists/Discovery/Web-Content/common.txt

This revealed a .htaccess file containing the last fragment:

legacy config
[5/5]-S

Part 5/5 = S
________________________________________
🏁 Final Flag Assembly

Now we concatenate all 5 parts in order:

S3GM + 3NT_ + F0R3 + NS1C + S

👉 Final Flag:

flag{S3GM3NT_F0R3NS1CS}
________________________________________
🔑 Key Learnings

•	Always inspect HTML comments and inline notes.

•	CSS & JS often hide developer build artifacts.

•	robots.txt leaks restricted/legacy paths.

•	Use tools like ffuf to brute-force hidden files (.htaccess, etc.).

•	Don’t fall for decoy code — look carefully at developer scratchpads.



