# Nom Nom Nom
> Some memories hide between the lines. Check the margins.

Given a zip file, first extract it.
<img width="264" height="125" alt="image" src="https://github.com/user-attachments/assets/fffac4e3-b44f-43ec-bb7f-ba8a4edcdcc7" />

As the category is Steganography, use:
```bash
exiftool old_photo.jpg
```
<img width="635" height="72" alt="image" src="https://github.com/user-attachments/assets/418fd790-6af8-4cff-9a13-2bae43e371d4" />

There was base64 string in user comments
`Rk1ZU01MQ0FOQjVXWTJKRU9aU0hZNVJFTk5XRUU9PT0=`

This give a base32 string
`FMYSMLCANB5WY2JEOZSHY5RENNWEE===`

Decoding this strings gives a ROT 47 decoded strings, decode it using brute-force method

The final flag is :
```bash
flag{EXIF_SAYS_HI}
```
