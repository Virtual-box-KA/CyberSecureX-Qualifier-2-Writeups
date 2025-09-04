# CTF Challenge Writeup: Layers of Silence

**Challenge Name:** Layers of Silence  
**Points:** 200

---

## Challenge Description
The challenge provided a compressed file `banner.png.gz` with a hint:

> "The file seems ordinary, yet it refuses to speak. Sometimes you need to peel away the outer shell, and sometimes you must listen where the noise is thinnest."

The goal was to extract hidden information and retrieve the CTF flag.

---

## Step-by-Step Solution

### Step 1: Extract the PNG
The file `banner.png.gz` was a Gzip-compressed file. We decompressed it using:

```bash
gzip -d banner.png.gz
```

This produced `banner.png`.

---

### Step 2: Analyze the PNG for Hidden Data
Based on the hint, we suspected steganography. We used **zsteg** to check for hidden data:

```bash
zsteg banner.png
```

Output revealed a hidden **Base58** string:

```
9pv9mpQrxmk3PrrpCBmywzGjti
```

---

### Step 3: Base58 Decoding
We decoded the string using Python:

```python
import base58

encoded = "9pv9mpQrxmk3PrrpCBmywzGjti"
decoded_bytes = base58.b58decode(encoded)
print(decoded_bytes)
```

Output:
```
b'06+1E{|mzmw){mkzm|G'
```

---

### Step 4: Recognize the Cipher
The decoded bytes were unreadable. The hint suggested a **shift cipher**. We attempted all possible shifts:

```python
for shift in range(0, 256):
    shifted = bytes((b + shift) % 256 for b in decoded_bytes)
    try:
        print(f"Shift {shift}: {shifted.decode()}")
    except:
        continue
```

---

### Step 5: Find the Correct Shift
Testing all shifts revealed that **Shift 40** produced meaningful text:

```
Shift 40: STEREOSECRET
```

---

### Step 6: Format the Flag
CTF flags usually follow the format `flag{...}`. Wrapping the decoded text:

```
flag{STEREO_SECRET}
```
