# Fractured Truth

Fellas, a zip *"tiles.7z"* is gives
Let us first unzip it.

8 Images, Seems like parts of a qr code.

Let us try to reassamble them, images seem to be parts of quadrant, 2 images per quadrant, I renamed them for my ease

<img width="1063" height="321" alt="image" src="https://github.com/user-attachments/assets/ce8121dd-c306-408e-8154-9b8053f9759e" />

I am a lazy person, I created a python script to do this

```python
  from PIL import Image

# Load your 4 PNG images (replace with actual image file paths)
TL1 = Image.open('TL1.png')
TL2 = Image.open('TL2.png')
TR1 = Image.open('TR1.png')
TR2 = Image.open('TR2.png')
LL1 = Image.open('LL1.png')
LL2 = Image.open('LL2.png')
RL1 = Image.open('RL1.png')
RL2 = Image.open('RL2.png')

# Create a function to generate a single image based on quadrant choices
def generate_image(tl, tr, ll, rl):
    # Concatenate the images for TL, TR, LL, RL quadrants
    TL = tl
    TR = tr
    LL = ll
    RL = rl

    # Calculate the final image size
    final_width = TL.width + TR.width
    final_height = TL.height + LL.height

    # Create a new blank image with the calculated size
    final_image = Image.new('RGBA', (final_width, final_height))

    # Paste each quadrant image into the final image
    final_image.paste(TL, (0, 0))
    final_image.paste(TR, (TL.width, 0))
    final_image.paste(LL, (0, TL.height))
    final_image.paste(RL, (TL.width, TL.height))

    return final_image

# List all possible combinations of quadrants (TL, TR, LL, RL)
combinations = [
    (TL1, TR1, LL1, RL1),
    (TL1, TR1, LL1, RL2),
    (TL1, TR1, LL2, RL1),
    (TL1, TR1, LL2, RL2),
    (TL1, TR2, LL1, RL1),
    (TL1, TR2, LL1, RL2),
    (TL1, TR2, LL2, RL1),
    (TL1, TR2, LL2, RL2),
    (TL2, TR1, LL1, RL1),
    (TL2, TR1, LL1, RL2),
    (TL2, TR1, LL2, RL1),
    (TL2, TR1, LL2, RL2),
    (TL2, TR2, LL1, RL1),
    (TL2, TR2, LL1, RL2),
    (TL2, TR2, LL2, RL1),
    (TL2, TR2, LL2, RL2)
]

# Generate and save each combination as a separate image
for i, combo in enumerate(combinations):
    final_image = generate_image(*combo)
    final_image.save(f'final_image_{i+1}.png')
    final_image.show()  # Optional, to show each generated image
    print(f"Generated and saved final_image_{i+1}.png")
```

Ohh nice, Got 12 Qrs. Most of them unsable but one

<img width="263" height="263" alt="image" src="https://github.com/user-attachments/assets/3fb8538c-66f2-47f4-b0dc-ba7fcbafefba" />

Just scan it with any qr scanner

The final flag is 
```bash
flag{puzzl3d_qr_c0mpl3t3}
```

