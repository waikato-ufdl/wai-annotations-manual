# Label distribution for image classification dataset

The following generates a label distribution (using percentages)
for the [17flowers]() image classification dataset, saving the 
result in a JSON file:

```bash
wai-annotations convert \
  from-subdir-ic \
    -i "./17flowers-subdir/subdir/**/*.jpg" \
  label-dist-ic \
    -f json \
    -o ./17flowers-labeldist-ic.json
```

The JSON file will look something like this:

```json
{
  "Windflower": 63,
  "Fritillary": 65,
  "Tigerlily": 50,
  "Tulip": 41,
  "Daffodil": 71,
  "Crocus": 50,
  "Sunflower": 71,
  "Buttercup": 54,
  "Daisy": 57,
  "Bluebell": 28,
  "Snowdrop": 50,
  "Dandelion": 43,
  "ColtsFoot": 55,
  "Iris": 77,
  "Pansy": 56,
  "LilyValley": 17
}
```

# Label distribution for object detection dataset

The following generates a label distribution (using percentages)
for the [17flowers]() object detection dataset, saving the 
result in a JSON file:

```bash
wai-annotations convert \
  from-voc-od \
    -i "./17flowers-voc/voc/*.xml" \
  label-dist-od \
    -f json \
    -p \
    -o ./17flowers-labeldist-od.json
```

The JSON file look similar to this:

```json
{
  "Daffodil": 8.372641509433961,
  "Pansy": 6.60377358490566,
  "Buttercup": 6.367924528301887,
  "Tigerlily": 5.89622641509434,
  "Daisy": 6.721698113207547,
  "Bluebell": 3.30188679245283,
  "Tulip": 4.834905660377359,
  "Iris": 9.080188679245282,
  "Fritillary": 7.665094339622641,
  "Dandelion": 5.070754716981132,
  "ColtsFoot": 6.485849056603773,
  "Crocus": 5.89622641509434,
  "Sunflower": 8.372641509433961,
  "Snowdrop": 5.89622641509434,
  "Windflower": 7.429245283018868,
  "LilyValley": 2.0047169811320753
}
```
