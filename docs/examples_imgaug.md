The following command-line loads ADAMS annotations and saves augmented MSCOCO ones.
The pipeline adds augmented images (`-m add`) that are cropped, flipped, blurred,
rotated and scaled. Each inline stream processor changes randomly about 10% of the
images (`-T 0.9` - if a random number between 0 and 1 is at least the threshold
provided with the `-T` parameter then the augmentation occurs). Since each 
augmentation has its own stochastic element, it is being seeded (`-a`) to generate 
reproducible datasets:

```bash
wai-annotations convert \
    from-adams-od \
      -i "input/**/*.report" \
    crop \
      -a -m add -T 0.9 -f 0.0 -t 0.1 \        # crop 0-10% of the image
    flip \
      -a -m add -T 0.9 -d lr \                # flip left-to-right
    gaussian-blur \
      -a -m add -T 0.9 -f 0.2 -t 0.5 \        # sigma from 0.2-0.5
    rotate \
      -a -m add -T 0.9 -f=-10 -t=10 \         # rotate from -10 to +10 degrees
    scale \
      -a -m add -T 0.9 -f 0.8 -t 1.2 -k -u \  # scale from 80 to 120%, keeping aspect ratio, resizing the image
    to-coco-od \
      -o output/annotations.json    
```
