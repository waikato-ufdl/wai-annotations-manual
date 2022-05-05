# Plugins
## Source stage
### FROM-ADAMS-IC
Reads image classification annotations in the ADAMS report-format

#### Domain(s):
- **Image Classification Domain**

#### Options:
```
usage: from-adams-ic [-I FILENAME] [-i FILENAME] [-N FILENAME] [-n FILENAME] [-o FILENAME] [--seed SEED] [-e FORMAT FORMAT FORMAT] -c FIELD

optional arguments:
  -I FILENAME, --inputs-file FILENAME
                        Files containing lists of input files (can use glob syntax)
  -i FILENAME, --input FILENAME
                        Input files (can use glob syntax)
  -N FILENAME, --negatives-file FILENAME
                        Files containing lists of negative files (can use glob syntax)
  -n FILENAME, --negative FILENAME
                        Files that have no annotations (can use glob syntax)
  -o FILENAME, --output-file FILENAME
                        optional file to write read filenames into
  --seed SEED           the seed to use for randomisation
  -e FORMAT FORMAT FORMAT, --extensions FORMAT FORMAT FORMAT
                        image format extensions in order of preference
  -c FIELD, --class-field FIELD
                        the report field containing the image class
```

### FROM-ADAMS-OD
Reads image object-detection annotations in the ADAMS report-format

#### Domain(s):
- **Image Object-Detection Domain**

#### Options:
```
usage: from-adams-od [-I FILENAME] [-i FILENAME] [-N FILENAME] [-n FILENAME] [-o FILENAME] [--seed SEED] [-e FORMAT FORMAT FORMAT] [-p PREFIXES [PREFIXES ...]]

optional arguments:
  -I FILENAME, --inputs-file FILENAME
                        Files containing lists of input files (can use glob syntax)
  -i FILENAME, --input FILENAME
                        Input files (can use glob syntax)
  -N FILENAME, --negatives-file FILENAME
                        Files containing lists of negative files (can use glob syntax)
  -n FILENAME, --negative FILENAME
                        Files that have no annotations (can use glob syntax)
  -o FILENAME, --output-file FILENAME
                        optional file to write read filenames into
  --seed SEED           the seed to use for randomisation
  -e FORMAT FORMAT FORMAT, --extensions FORMAT FORMAT FORMAT
                        image format extensions in order of preference
  -p PREFIXES [PREFIXES ...], --prefixes PREFIXES [PREFIXES ...]
                        prefixes to parse
```

### FROM-BLUE-CHANNEL-IS
Reads image segmentation files in the blue-channel format

#### Domain(s):
- **Image Segmentation Domain**

#### Options:
```
usage: from-blue-channel-is [-I FILENAME] [-i FILENAME] [-N FILENAME] [-n FILENAME] [-o FILENAME] [--seed SEED] [--image-path-rel PATH] --labels LABEL [LABEL ...]

optional arguments:
  -I FILENAME, --inputs-file FILENAME
                        Files containing lists of input files (can use glob syntax)
  -i FILENAME, --input FILENAME
                        Input files (can use glob syntax)
  -N FILENAME, --negatives-file FILENAME
                        Files containing lists of negative files (can use glob syntax)
  -n FILENAME, --negative FILENAME
                        Files that have no annotations (can use glob syntax)
  -o FILENAME, --output-file FILENAME
                        optional file to write read filenames into
  --seed SEED           the seed to use for randomisation
  --image-path-rel PATH
                        Relative path to image files from annotations
  --labels LABEL [LABEL ...]
                        specifies the labels for each index
```

### FROM-COCO-OD
Reads image object-detection annotations in the MS-COCO JSON-format

#### Domain(s):
- **Image Object-Detection Domain**

#### Options:
```
usage: from-coco-od [-I FILENAME] [-i FILENAME] [-N FILENAME] [-n FILENAME] [-o FILENAME] [--seed SEED]

optional arguments:
  -I FILENAME, --inputs-file FILENAME
                        Files containing lists of input files (can use glob syntax)
  -i FILENAME, --input FILENAME
                        Input files (can use glob syntax)
  -N FILENAME, --negatives-file FILENAME
                        Files containing lists of negative files (can use glob syntax)
  -n FILENAME, --negative FILENAME
                        Files that have no annotations (can use glob syntax)
  -o FILENAME, --output-file FILENAME
                        optional file to write read filenames into
  --seed SEED           the seed to use for randomisation
```

### FROM-COMMON-VOICE-SP
Reads speech transcriptions in the Mozilla Common-Voice TSV-format

#### Domain(s):
- **Speech Domain**

#### Options:
```
usage: from-common-voice-sp [-I FILENAME] [-i FILENAME] [-N FILENAME] [-n FILENAME] [-o FILENAME] [--seed SEED] [--rel-path REL_PATH]

optional arguments:
  -I FILENAME, --inputs-file FILENAME
                        Files containing lists of input files (can use glob syntax)
  -i FILENAME, --input FILENAME
                        Input files (can use glob syntax)
  -N FILENAME, --negatives-file FILENAME
                        Files containing lists of negative files (can use glob syntax)
  -n FILENAME, --negative FILENAME
                        Files that have no annotations (can use glob syntax)
  -o FILENAME, --output-file FILENAME
                        optional file to write read filenames into
  --seed SEED           the seed to use for randomisation
  --rel-path REL_PATH   the relative path from the annotations file to the audio files
```

### FROM-FESTVOX-SP
Reads speech transcriptions in the Festival FestVox format

#### Domain(s):
- **Speech Domain**

#### Options:
```
usage: from-festvox-sp [-I FILENAME] [-i FILENAME] [-N FILENAME] [-n FILENAME] [-o FILENAME] [--seed SEED] [--rel-path REL_PATH]

optional arguments:
  -I FILENAME, --inputs-file FILENAME
                        Files containing lists of input files (can use glob syntax)
  -i FILENAME, --input FILENAME
                        Input files (can use glob syntax)
  -N FILENAME, --negatives-file FILENAME
                        Files containing lists of negative files (can use glob syntax)
  -n FILENAME, --negative FILENAME
                        Files that have no annotations (can use glob syntax)
  -o FILENAME, --output-file FILENAME
                        optional file to write read filenames into
  --seed SEED           the seed to use for randomisation
  --rel-path REL_PATH   the relative path from the annotations file to the audio files
```

### FROM-INDEXED-PNG-IS
Reads image segmentation files in the indexed-PNG format

#### Domain(s):
- **Image Segmentation Domain**

#### Options:
```
usage: from-indexed-png-is [-I FILENAME] [-i FILENAME] [-N FILENAME] [-n FILENAME] [-o FILENAME] [--seed SEED] [--image-path-rel PATH] --labels LABEL [LABEL ...]

optional arguments:
  -I FILENAME, --inputs-file FILENAME
                        Files containing lists of input files (can use glob syntax)
  -i FILENAME, --input FILENAME
                        Input files (can use glob syntax)
  -N FILENAME, --negatives-file FILENAME
                        Files containing lists of negative files (can use glob syntax)
  -n FILENAME, --negative FILENAME
                        Files that have no annotations (can use glob syntax)
  -o FILENAME, --output-file FILENAME
                        optional file to write read filenames into
  --seed SEED           the seed to use for randomisation
  --image-path-rel PATH
                        Relative path to image files from annotations
  --labels LABEL [LABEL ...]
                        specifies the labels for each index
```

### FROM-LAYER-SEGMENTS-IS
Reads in the layer-segments image-segmentation format from disk, where each label has a binary PNG storing the mask for that label

#### Domain(s):
- **Image Segmentation Domain**

#### Options:
```
usage: from-layer-segments-is [-I FILENAME] [-i FILENAME] [-N FILENAME] [-n FILENAME] [-o FILENAME] [--seed SEED] [--label-separator SEPARATOR] --labels LABEL [LABEL ...] [--image-path-rel PATH]

optional arguments:
  -I FILENAME, --inputs-file FILENAME
                        Files containing lists of input files (can use glob syntax)
  -i FILENAME, --input FILENAME
                        Input files (can use glob syntax)
  -N FILENAME, --negatives-file FILENAME
                        Files containing lists of negative files (can use glob syntax)
  -n FILENAME, --negative FILENAME
                        Files that have no annotations (can use glob syntax)
  -o FILENAME, --output-file FILENAME
                        optional file to write read filenames into
  --seed SEED           the seed to use for randomisation
  --label-separator SEPARATOR
                        the separator between the base filename and the label
  --labels LABEL [LABEL ...]
                        specifies the labels for each index
  --image-path-rel PATH
                        Relative path to image files from annotations
```

### FROM-ROI-OD
Reads image object-detection annotations in the ROI CSV-format

#### Domain(s):
- **Image Object-Detection Domain**

#### Options:
```
usage: from-roi-od [-I FILENAME] [-i FILENAME] [-N FILENAME] [-n FILENAME] [-o FILENAME] [--seed SEED] [-e FORMAT FORMAT FORMAT] [--prefix READER_PREFIX] [--suffix READER_SUFFIX]

optional arguments:
  -I FILENAME, --inputs-file FILENAME
                        Files containing lists of input files (can use glob syntax)
  -i FILENAME, --input FILENAME
                        Input files (can use glob syntax)
  -N FILENAME, --negatives-file FILENAME
                        Files containing lists of negative files (can use glob syntax)
  -n FILENAME, --negative FILENAME
                        Files that have no annotations (can use glob syntax)
  -o FILENAME, --output-file FILENAME
                        optional file to write read filenames into
  --seed SEED           the seed to use for randomisation
  -e FORMAT FORMAT FORMAT, --extensions FORMAT FORMAT FORMAT
                        image format extensions in order of preference
  --prefix READER_PREFIX
                        the prefix for output filenames (default = '')
  --suffix READER_SUFFIX
                        the suffix for output filenames (default = '-rois.csv')
```

### FROM-SUBDIR-IC
Reads images from sub-directories named after their class labels.

#### Domain(s):
- **Image Classification Domain**

#### Options:
```
usage: from-subdir-ic [-I FILENAME] [-i FILENAME] [-N FILENAME] [-n FILENAME] [-o FILENAME] [--seed SEED]

optional arguments:
  -I FILENAME, --inputs-file FILENAME
                        Files containing lists of input files (can use glob syntax)
  -i FILENAME, --input FILENAME
                        Input files (can use glob syntax)
  -N FILENAME, --negatives-file FILENAME
                        Files containing lists of negative files (can use glob syntax)
  -n FILENAME, --negative FILENAME
                        Files that have no annotations (can use glob syntax)
  -o FILENAME, --output-file FILENAME
                        optional file to write read filenames into
  --seed SEED           the seed to use for randomisation
```

### FROM-TF-OD
Reads image object-detection annotations in the TFRecords binary format

#### Domain(s):
- **Image Object-Detection Domain**

#### Options:
```
usage: from-tf-od [-I FILENAME] [-i FILENAME] [-N FILENAME] [-n FILENAME] [-o FILENAME] [--seed SEED] [--mask-threshold THRESHOLD] [--sample-stride STRIDE]

optional arguments:
  -I FILENAME, --inputs-file FILENAME
                        Files containing lists of input files (can use glob syntax)
  -i FILENAME, --input FILENAME
                        Input files (can use glob syntax)
  -N FILENAME, --negatives-file FILENAME
                        Files containing lists of negative files (can use glob syntax)
  -n FILENAME, --negative FILENAME
                        Files that have no annotations (can use glob syntax)
  -o FILENAME, --output-file FILENAME
                        optional file to write read filenames into
  --seed SEED           the seed to use for randomisation
  --mask-threshold THRESHOLD
                        the threshold to use when calculating polygons from masks
  --sample-stride STRIDE
                        the stride to use when calculating polygons from masks
```

### FROM-VGG-OD
Reads image object-detection annotations in the VGG JSON-format

#### Domain(s):
- **Image Object-Detection Domain**

#### Options:
```
usage: from-vgg-od [-I FILENAME] [-i FILENAME] [-N FILENAME] [-n FILENAME] [-o FILENAME] [--seed SEED]

optional arguments:
  -I FILENAME, --inputs-file FILENAME
                        Files containing lists of input files (can use glob syntax)
  -i FILENAME, --input FILENAME
                        Input files (can use glob syntax)
  -N FILENAME, --negatives-file FILENAME
                        Files containing lists of negative files (can use glob syntax)
  -n FILENAME, --negative FILENAME
                        Files that have no annotations (can use glob syntax)
  -o FILENAME, --output-file FILENAME
                        optional file to write read filenames into
  --seed SEED           the seed to use for randomisation
```

### FROM-VIDEO-FILE-OD
Reads frames from a video file.

#### Domain(s):
- **Image Object-Detection Domain**

#### Options:
```
usage: from-video-file-od [-f FROM_FRAME] [-i INPUT_FILE] [-m MAX_FRAMES] [-n NTH_FRAME] [-p PREFIX] [-t TO_FRAME]

optional arguments:
  -f FROM_FRAME, --from-frame FROM_FRAME
                        determines with which frame to start the stream (1-based index)
  -i INPUT_FILE, --input INPUT_FILE
                        the video file to read
  -m MAX_FRAMES, --max-frames MAX_FRAMES
                        determines the maximum number of frames to read; ignored if <=0
  -n NTH_FRAME, --nth-frame NTH_FRAME
                        determines whether frames get skipped and only evert nth frame gets forwarded
  -p PREFIX, --prefix PREFIX
                        the prefix to use for the frames
  -t TO_FRAME, --to-frame TO_FRAME
                        determines after which frame to stop (1-based index); ignored if <=0
```

### FROM-VOC-OD
Reads image object-detection annotations in the Pascal VOC XML-format

#### Domain(s):
- **Image Object-Detection Domain**

#### Options:
```
usage: from-voc-od [-I FILENAME] [-i FILENAME] [-N FILENAME] [-n FILENAME] [-o FILENAME] [--seed SEED]

optional arguments:
  -I FILENAME, --inputs-file FILENAME
                        Files containing lists of input files (can use glob syntax)
  -i FILENAME, --input FILENAME
                        Input files (can use glob syntax)
  -N FILENAME, --negatives-file FILENAME
                        Files containing lists of negative files (can use glob syntax)
  -n FILENAME, --negative FILENAME
                        Files that have no annotations (can use glob syntax)
  -o FILENAME, --output-file FILENAME
                        optional file to write read filenames into
  --seed SEED           the seed to use for randomisation
```

### FROM-WEBCAM-OD
Reads frames from a webcam.

#### Domain(s):
- **Image Object-Detection Domain**

#### Options:
```
usage: from-webcam-od [-f FROM_FRAME] [-m MAX_FRAMES] [-n NTH_FRAME] [-p PREFIX] [-t TO_FRAME] [-i WEBCAM_ID]

optional arguments:
  -f FROM_FRAME, --from-frame FROM_FRAME
                        determines with which frame to start the stream (1-based index)
  -m MAX_FRAMES, --max-frames MAX_FRAMES
                        determines the maximum number of frames to read; ignored if <=0
  -n NTH_FRAME, --nth-frame NTH_FRAME
                        determines whether frames get skipped and only evert nth frame gets forwarded
  -p PREFIX, --prefix PREFIX
                        the prefix to use for the frames
  -t TO_FRAME, --to-frame TO_FRAME
                        determines after which frame to stop (1-based index); ignored if <=0
  -i WEBCAM_ID, --webcam-id WEBCAM_ID
                        the webcam ID to read from
```

### FROM-YOLO-OD
Reads image object-detection annotations in the YOLO format

#### Domain(s):
- **Image Object-Detection Domain**

#### Options:
```
usage: from-yolo-od [-I FILENAME] [-i FILENAME] [-N FILENAME] [-n FILENAME] [-o FILENAME] [--seed SEED] [--image-path-rel PATH] [-l PATH]

optional arguments:
  -I FILENAME, --inputs-file FILENAME
                        Files containing lists of input files (can use glob syntax)
  -i FILENAME, --input FILENAME
                        Input files (can use glob syntax)
  -N FILENAME, --negatives-file FILENAME
                        Files containing lists of negative files (can use glob syntax)
  -n FILENAME, --negative FILENAME
                        Files that have no annotations (can use glob syntax)
  -o FILENAME, --output-file FILENAME
                        optional file to write read filenames into
  --seed SEED           the seed to use for randomisation
  --image-path-rel PATH
                        Relative path to image files from annotations
  -l PATH, --labels PATH
                        Path to the labels file
```


## Processor stage
### ADD-ANNOTATION-OVERLAY-OD
Adds object detection overlays to images passing through.

#### Domain(s):
- **Image Object-Detection Domain**

#### Options:
```
usage: add-annotation-overlay-od [--fill] [--fill-alpha FILL_ALPHA] [--font-family FONT_FAMILY] [--font-size FONT_SIZE] [--force-bbox] [--label-key LABEL_KEY] [--labels LABELS] [--num-decimals NUM_DECIMALS] [--outline-alpha OUTLINE_ALPHA] [--outline-thickness OUTLINE_THICKNESS] [--text-format TEXT_FORMAT] [--text-placement TEXT_PLACEMENT] [--vary-colors]

optional arguments:
  --fill                whether to fill the bounding boxes/polygons
  --fill-alpha FILL_ALPHA
                        the alpha value to use for the filling.
  --font-family FONT_FAMILY
                        the name of the TTF font-family to use, note: any hyphens need escaping with backslash.
  --font-size FONT_SIZE
                        the size of the font.
  --force-bbox          whether to force a bounding box even if there is a polygon available
  --label-key LABEL_KEY
                        the key in the meta-data that contains the label.
  --labels LABELS       the comma-separated list of labels of annotations to overlay, leave empty to overlay all
  --num-decimals NUM_DECIMALS
                        the number of decimals to use for float numbers in the text format string.
  --outline-alpha OUTLINE_ALPHA
                        the alpha value to use for the outline.
  --outline-thickness OUTLINE_THICKNESS
                        the line thickness to use for the outline, <1 to turn off.
  --text-format TEXT_FORMAT
                        template for the text to print on top of the bounding box or polygon, '{PH}' is a placeholder for the 'PH' value from the meta-data or 'label' for the current label; ignored if empty.
  --text-placement TEXT_PLACEMENT
                        comma-separated list of vertical (T=top, C=center, B=bottom) and horizontal (L=left, C=center, R=right) anchoring.
  --vary-colors         whether to vary the colors of the outline/filling regardless of label
```

### CHECK-DUPLICATE-FILENAMES
Causes the conversion stream to halt when multiple dataset items have the same filename

#### Domain(s):
- **Speech Domain**
- **Image Object-Detection Domain**
- **Image Segmentation Domain**
- **Image Classification Domain**

#### Options:
```
usage: check-duplicate-filenames
```

### COERCE-BOX
Converts all annotation bounds into box regions

#### Domain(s):
- **Image Object-Detection Domain**

#### Options:
```
usage: coerce-box
```

### COERCE-MASK
Converts all annotation bounds into polygon regions

#### Domain(s):
- **Image Object-Detection Domain**

#### Options:
```
usage: coerce-mask
```

### CONVERT-IMAGE-FORMAT
Converts images from one format to another

#### Domain(s):
- **Image Object-Detection Domain**
- **Image Segmentation Domain**
- **Image Classification Domain**

#### Options:
```
usage: convert-image-format -f FORMAT

optional arguments:
  -f FORMAT, --format FORMAT
                        format to convert images to
```

### CROP
Crops images.

#### Domain(s):
- **Image Object-Detection Domain**
- **Image Classification Domain**

#### Options:
```
usage: crop [-m IMGAUG_MODE] [--suffix IMGAUG_SUFFIX] [-f PERCENT_FROM] [-t PERCENT_TO] [-s SEED] [-a] [-T THRESHOLD] [-u]

optional arguments:
  -m IMGAUG_MODE, --mode IMGAUG_MODE
                        the image augmentation mode to use, available modes: replace, add
  --suffix IMGAUG_SUFFIX
                        the suffix to use for the file names in case of augmentation mode add
  -f PERCENT_FROM, --from-percent PERCENT_FROM
                        the minimum percent to crop from images
  -t PERCENT_TO, --to-percent PERCENT_TO
                        the maximum percent to crop from images
  -s SEED, --seed SEED  the seed value to use for the random number generator; randomly seeded if not provided
  -a, --seed-augmentation
                        whether to seed the augmentation; if specified, uses the seeded random generator to produce a seed value from 0 to 1000 for the augmentation.
  -T THRESHOLD, --threshold THRESHOLD
                        the threshold to use for Random.rand(): if equal or above, augmentation gets applied; range: 0-1; default: 0 (= always)
  -u, --update-size     whether to update the image size after the crop operation or scale back to original size
```

### DIMENSION-DISCARDER
Removes annotations which fall outside certain size constraints

#### Domain(s):
- **Image Object-Detection Domain**

#### Options:
```
usage: dimension-discarder [--max-area MAX_AREA] [--max-height MAX_HEIGHT] [--max-width MAX_WIDTH] [--min-area MIN_AREA] [--min-height MIN_HEIGHT] [--min-width MIN_WIDTH] [--verbose]

optional arguments:
  --max-area MAX_AREA   the maximum area of annotations to convert
  --max-height MAX_HEIGHT
                        the maximum height of annotations to convert
  --max-width MAX_WIDTH
                        the maximum width of annotations to convert
  --min-area MIN_AREA   the minimum area of annotations to convert
  --min-height MIN_HEIGHT
                        the minimum height of annotations to convert
  --min-width MIN_WIDTH
                        the minimum width of annotations to convert
  --verbose             outputs information when discarding annotations
```

### DISCARD-NEGATIVES
Discards negative examples (those without annotations) from the stream

#### Domain(s):
- **Speech Domain**
- **Image Object-Detection Domain**
- **Image Segmentation Domain**
- **Image Classification Domain**

#### Options:
```
usage: discard-negatives
```

### DROP-FRAMES
Drops frames from the stream.

#### Domain(s):
- **Image Object-Detection Domain**
- **Image Segmentation Domain**
- **Image Classification Domain**

#### Options:
```
usage: drop-frames [-n NTH_FRAME]

optional arguments:
  -n NTH_FRAME, --nth-frame NTH_FRAME
                        which nth frame to drop, e..g, '2' means to drop every 2nd frame; passes frames through if <=1
```

### FILTER-LABELS
Filters detected objects down to those with specified labels.

#### Domain(s):
- **Image Object-Detection Domain**

#### Options:
```
usage: filter-labels [-l LABELS [LABELS ...]] [-r regexp]

optional arguments:
  -l LABELS [LABELS ...], --labels LABELS [LABELS ...]
                        labels to use
  -r regexp, --regexp regexp
                        regular expression for using only a subset of labels
```

### FLIP
Flips images either left-to-right, up-to-down or both.

#### Domain(s):
- **Image Object-Detection Domain**
- **Image Classification Domain**

#### Options:
```
usage: flip [-d DIRECTION] [-m IMGAUG_MODE] [--suffix IMGAUG_SUFFIX] [-s SEED] [-a] [-T THRESHOLD]

optional arguments:
  -d DIRECTION, --direction DIRECTION
                        the direction to flip, available options: lr, up, lrup
  -m IMGAUG_MODE, --mode IMGAUG_MODE
                        the image augmentation mode to use, available modes: replace, add
  --suffix IMGAUG_SUFFIX
                        the suffix to use for the file names in case of augmentation mode add
  -s SEED, --seed SEED  the seed value to use for the random number generator; randomly seeded if not provided
  -a, --seed-augmentation
                        whether to seed the augmentation; if specified, uses the seeded random generator to produce a seed value from 0 to 1000 for the augmentation.
  -T THRESHOLD, --threshold THRESHOLD
                        the threshold to use for Random.rand(): if equal or above, augmentation gets applied; range: 0-1; default: 0 (= always)
```

### GAUSSIAN-BLUR
Applies gaussian blur to images.

#### Domain(s):
- **Image Object-Detection Domain**
- **Image Classification Domain**

#### Options:
```
usage: gaussian-blur [-m IMGAUG_MODE] [--suffix IMGAUG_SUFFIX] [-s SEED] [-a] [-f SIGMA_FROM] [-t SIGMA_TO] [-T THRESHOLD]

optional arguments:
  -m IMGAUG_MODE, --mode IMGAUG_MODE
                        the image augmentation mode to use, available modes: replace, add
  --suffix IMGAUG_SUFFIX
                        the suffix to use for the file names in case of augmentation mode add
  -s SEED, --seed SEED  the seed value to use for the random number generator; randomly seeded if not provided
  -a, --seed-augmentation
                        whether to seed the augmentation; if specified, uses the seeded random generator to produce a seed value from 0 to 1000 for the augmentation.
  -f SIGMA_FROM, --from-sigma SIGMA_FROM
                        the minimum sigma for the blur to apply to the images
  -t SIGMA_TO, --to-sigma SIGMA_TO
                        the maximum sigma for the blur to apply to the images
  -T THRESHOLD, --threshold THRESHOLD
                        the threshold to use for Random.rand(): if equal or above, augmentation gets applied; range: 0-1; default: 0 (= always)
```

### HSL-GRAYSCALE
Turns RGB images into fake grayscale ones by converting them to HSL and then using the L channel for all channels. The brightness can be influenced and varied even.

#### Domain(s):
- **Image Object-Detection Domain**
- **Image Classification Domain**

#### Options:
```
usage: hsl-grayscale [-f FACTOR_FROM] [-t FACTOR_TO] [-m IMGAUG_MODE] [--suffix IMGAUG_SUFFIX] [-s SEED] [-a] [-T THRESHOLD]

optional arguments:
  -f FACTOR_FROM, --from-factor FACTOR_FROM
                        the start of the factor range to apply to the L channel to darken or lighten the image (<1: darker, >1: lighter)
  -t FACTOR_TO, --to-factor FACTOR_TO
                        the end of the factor range to apply to the L channel to darken or lighten the image (<1: darker, >1: lighter)
  -m IMGAUG_MODE, --mode IMGAUG_MODE
                        the image augmentation mode to use, available modes: replace, add
  --suffix IMGAUG_SUFFIX
                        the suffix to use for the file names in case of augmentation mode add
  -s SEED, --seed SEED  the seed value to use for the random number generator; randomly seeded if not provided
  -a, --seed-augmentation
                        whether to seed the augmentation; if specified, uses the seeded random generator to produce a seed value from 0 to 1000 for the augmentation.
  -T THRESHOLD, --threshold THRESHOLD
                        the threshold to use for Random.rand(): if equal or above, augmentation gets applied; range: 0-1; default: 0 (= always)
```

### LINEAR-CONTRAST
Applies linear contrast to images.

#### Domain(s):
- **Image Object-Detection Domain**
- **Image Classification Domain**

#### Options:
```
usage: linear-contrast [-f ALPHA_FROM] [-t ALPHA_TO] [-m IMGAUG_MODE] [--suffix IMGAUG_SUFFIX] [-s SEED] [-a] [-T THRESHOLD]

optional arguments:
  -f ALPHA_FROM, --from-alpha ALPHA_FROM
                        the minimum alpha to apply to the images
  -t ALPHA_TO, --to-alpha ALPHA_TO
                        the maximum alpha to apply to the images
  -m IMGAUG_MODE, --mode IMGAUG_MODE
                        the image augmentation mode to use, available modes: replace, add
  --suffix IMGAUG_SUFFIX
                        the suffix to use for the file names in case of augmentation mode add
  -s SEED, --seed SEED  the seed value to use for the random number generator; randomly seeded if not provided
  -a, --seed-augmentation
                        whether to seed the augmentation; if specified, uses the seeded random generator to produce a seed value from 0 to 1000 for the augmentation.
  -T THRESHOLD, --threshold THRESHOLD
                        the threshold to use for Random.rand(): if equal or above, augmentation gets applied; range: 0-1; default: 0 (= always)
```

### MAP-LABELS
Maps object-detection labels from one set to another

#### Domain(s):
- **Image Object-Detection Domain**

#### Options:
```
usage: map-labels [-m old=new]

optional arguments:
  -m old=new, --mapping old=new
                        mapping for labels, for replacing one label string with another (eg when fixing/collapsing labels)
```

### OD-TO-IC
Converts image object-detection instances into image classification instances

#### Domain(s):
- **Image Object-Detection Domain**

#### Options:
```
usage: od-to-ic [-m HANDLER]

optional arguments:
  -m HANDLER, --multiplicity HANDLER
                        how to handle instances with more than one located object
```

### OD-TO-IS
Converts image object-detection instances into image segmentation instances

#### Domain(s):
- **Image Object-Detection Domain**

#### Options:
```
usage: od-to-is [--label-error] --labels LABEL [LABEL ...]

optional arguments:
  --label-error         whether to raise errors when an unspecified label is encountered (default is to ignore)
  --labels LABEL [LABEL ...]
                        specifies the labels for each index
```

### PASSTHROUGH
Dummy ISP which has no effect on the conversion stream

#### Domain(s):
- **Speech Domain**
- **Image Object-Detection Domain**
- **Image Segmentation Domain**
- **Image Classification Domain**

#### Options:
```
usage: passthrough
```

### POLYGON-DISCARDER
Removes annotations with polygons which fall outside certain point limit constraints

#### Domain(s):
- **Image Object-Detection Domain**

#### Options:
```
usage: polygon-discarder [--max-points MAX_POINTS] [--min-points MIN_POINTS] [--verbose]

optional arguments:
  --max-points MAX_POINTS
                        the maximum number of points in the polygon
  --min-points MIN_POINTS
                        the minimum number of points in the polygon
  --verbose             outputs information when discarding annotations
```

### REMOVE-CLASSES
Removes classes from classification/image-segmentation instances

#### Domain(s):
- **Image Segmentation Domain**
- **Image Classification Domain**

#### Options:
```
usage: remove-classes -c CLASS [CLASS ...]

optional arguments:
  -c CLASS [CLASS ...], --classes CLASS [CLASS ...]
                        the classes to remove
```

### ROTATE
Rotates images randomly within a range of degrees or by a specified degree. Specify seed value and force augmentation to be seeded to generate repeatable augmentations.

#### Domain(s):
- **Image Object-Detection Domain**
- **Image Classification Domain**

#### Options:
```
usage: rotate [-f DEGREE_FROM] [-t DEGREE_TO] [-m IMGAUG_MODE] [--suffix IMGAUG_SUFFIX] [-s SEED] [-a] [-T THRESHOLD]

optional arguments:
  -f DEGREE_FROM, --from-degree DEGREE_FROM
                        the start of the degree range to use for rotating the images
  -t DEGREE_TO, --to-degree DEGREE_TO
                        the end of the degree range to use for rotating the images
  -m IMGAUG_MODE, --mode IMGAUG_MODE
                        the image augmentation mode to use, available modes: replace, add
  --suffix IMGAUG_SUFFIX
                        the suffix to use for the file names in case of augmentation mode add
  -s SEED, --seed SEED  the seed value to use for the random number generator; randomly seeded if not provided
  -a, --seed-augmentation
                        whether to seed the augmentation; if specified, uses the seeded random generator to produce a seed value from 0 to 1000 for the augmentation.
  -T THRESHOLD, --threshold THRESHOLD
                        the threshold to use for Random.rand(): if equal or above, augmentation gets applied; range: 0-1; default: 0 (= always)
```

### SCALE
Scales images randomly within a range of percentages or by a specified percentage. Specify seed value and force augmentation to be seeded to generate repeatable augmentations.

#### Domain(s):
- **Image Object-Detection Domain**
- **Image Classification Domain**

#### Options:
```
usage: scale [-m IMGAUG_MODE] [--suffix IMGAUG_SUFFIX] [-k] [-f PERCENTAGE_FROM] [-t PERCENTAGE_TO] [-s SEED] [-a] [-T THRESHOLD] [-u]

optional arguments:
  -m IMGAUG_MODE, --mode IMGAUG_MODE
                        the image augmentation mode to use, available modes: replace, add
  --suffix IMGAUG_SUFFIX
                        the suffix to use for the file names in case of augmentation mode add
  -k, --keep-aspect     whether to keep the aspect ratio
  -f PERCENTAGE_FROM, --from-percentage PERCENTAGE_FROM
                        the start of the percentage range to use for scaling the images
  -t PERCENTAGE_TO, --to-percentage PERCENTAGE_TO
                        the end of the percentage range to use for scaling the images
  -s SEED, --seed SEED  the seed value to use for the random number generator; randomly seeded if not provided
  -a, --seed-augmentation
                        whether to seed the augmentation; if specified, uses the seeded random generator to produce a seed value from 0 to 1000 for the augmentation.
  -T THRESHOLD, --threshold THRESHOLD
                        the threshold to use for Random.rand(): if equal or above, augmentation gets applied; range: 0-1; default: 0 (= always)
  -u, --update-size     whether to update the image size after the scaling operation or use original size
```

### SKIP-SIMILAR-FRAMES
Skips frames in the stream that are deemed too similar.

#### Domain(s):
- **Image Object-Detection Domain**
- **Image Segmentation Domain**
- **Image Classification Domain**

#### Options:
```
usage: skip-similar-frames [-b BW_THRESHOLD] [-t CHANGE_THRESHOLD] [-c CONVERSION] [-v]

optional arguments:
  -b BW_THRESHOLD, --bw-threshold BW_THRESHOLD
                        the threshold to use for converting a gray-scale like image to black and white (0-255)
  -t CHANGE_THRESHOLD, --change-threshold CHANGE_THRESHOLD
                        the percentage of pixels that changed relative to size of image (0-1)
  -c CONVERSION, --conversion CONVERSION
                        how to convert the BGR image to a single channel image (gray/r/g/b)
  -v, --verbose         whether to output some debugging output.
```

### STRIP-ANNOTATIONS
ISP which removes annotations from instances

#### Domain(s):
- **Speech Domain**
- **Image Object-Detection Domain**
- **Image Segmentation Domain**
- **Image Classification Domain**

#### Options:
```
usage: strip-annotations
```


## Sink stage
### CALC-FRAME-CHANGES
Calculates the changes between frames, which can be used with the skip-similar-frames ISP.

#### Domain(s):
- **Image Object-Detection Domain**

#### Options:
```
usage: calc-frame-changes [-b BW_THRESHOLD] [-t CHANGE_THRESHOLD] [-c CONVERSION] [-B NUM_BINS] [-o OUTPUT_FILE] [-f OUTPUT_FORMAT] [-v]

optional arguments:
  -b BW_THRESHOLD, --bw-threshold BW_THRESHOLD
                        the threshold to use for converting a gray-scale like image to black and white (0-255)
  -t CHANGE_THRESHOLD, --change-threshold CHANGE_THRESHOLD
                        the percentage of pixels that changed relative to size of image (0-1)
  -c CONVERSION, --conversion CONVERSION
                        how to convert the BGR image to a single channel image (gray/r/g/b)
  -B NUM_BINS, --num-bins NUM_BINS
                        the number of bins to use for the histogram
  -o OUTPUT_FILE, --output OUTPUT_FILE
                        the file to write to statistics to, stdout if not provided
  -f OUTPUT_FORMAT, --output-format OUTPUT_FORMAT
                        how to output the statistics (text/csv/json)
  -v, --verbose         whether to output some debugging output.
```

### LABEL-DIST-IC
Generates a label distribution.

#### Domain(s):
- **Image Classification Domain**

#### Options:
```
usage: label-dist-ic [-o OUTPUT_FILE] [-f OUTPUT_FORMAT] [-p]

optional arguments:
  -o OUTPUT_FILE, --output OUTPUT_FILE
                        the file to write the statistics to; uses stdout if omitted
  -f OUTPUT_FORMAT, --format OUTPUT_FORMAT
                        the format to use for the output, available modes: csv, json
  -p, --percentages     whether to output percentages instead of counts.
```

### LABEL-DIST-IS
Generates a label distribution.

#### Domain(s):
- **Image Segmentation Domain**

#### Options:
```
usage: label-dist-is [-o OUTPUT_FILE] [-f OUTPUT_FORMAT] [-p]

optional arguments:
  -o OUTPUT_FILE, --output OUTPUT_FILE
                        the file to write the statistics to; uses stdout if omitted
  -f OUTPUT_FORMAT, --format OUTPUT_FORMAT
                        the format to use for the output, available modes: csv, json
  -p, --percentages     whether to output percentages instead of counts.
```

### LABEL-DIST-OD
Generates a label distribution.

#### Domain(s):
- **Image Object-Detection Domain**

#### Options:
```
usage: label-dist-od [-o OUTPUT_FILE] [-f OUTPUT_FORMAT] [-p]

optional arguments:
  -o OUTPUT_FILE, --output OUTPUT_FILE
                        the file to write the statistics to; uses stdout if omitted
  -f OUTPUT_FORMAT, --format OUTPUT_FORMAT
                        the format to use for the output, available modes: csv, json
  -p, --percentages     whether to output percentages instead of counts.
```

### TO-ADAMS-IC
Writes image classification annotations in the ADAMS report-format

#### Domain(s):
- **Image Classification Domain**

#### Options:
```
usage: to-adams-ic -c FIELD [--annotations-only] -o PATH [--split-names SPLIT NAME [SPLIT NAME ...]] [--split-ratios RATIO [RATIO ...]]

optional arguments:
  -c FIELD, --class-field FIELD
                        the report field containing the image class
  --annotations-only    skip the writing of data files, outputting only the annotation files
  -o PATH, --output PATH
                        output directory to write files to
  --split-names SPLIT NAME [SPLIT NAME ...]
                        the names to use for the splits
  --split-ratios RATIO [RATIO ...]
                        the ratios to use for the splits
```

### TO-ADAMS-OD
Writes image object-detection annotations in the ADAMS report-format

#### Domain(s):
- **Image Object-Detection Domain**

#### Options:
```
usage: to-adams-od [--annotations-only] -o PATH [--split-names SPLIT NAME [SPLIT NAME ...]] [--split-ratios RATIO [RATIO ...]]

optional arguments:
  --annotations-only    skip the writing of data files, outputting only the annotation files
  -o PATH, --output PATH
                        output directory to write files to
  --split-names SPLIT NAME [SPLIT NAME ...]
                        the names to use for the splits
  --split-ratios RATIO [RATIO ...]
                        the ratios to use for the splits
```

### TO-ANNOTATION-OVERLAY-OD
Generates an image with all the annotation shapes (bbox or polygon) overlayed.

#### Domain(s):
- **Image Object-Detection Domain**

#### Options:
```
usage: to-annotation-overlay-od [-b BACKGROUND_COLOR] [-c COLOR] [-o OUTPUT_FILE] [-s SCALE_TO]

optional arguments:
  -b BACKGROUND_COLOR, --background-color BACKGROUND_COLOR
                        the color to use for the background as RGBA byte-quadruplet, e.g.: 255,255,255,255
  -c COLOR, --color COLOR
                        the color to use for drawing the shapes as RGBA byte-quadruplet, e.g.: 255,0,0,64
  -o OUTPUT_FILE, --output OUTPUT_FILE
                        the PNG image to write the generated overlay to
  -s SCALE_TO, --scale-to SCALE_TO
                        the dimensions to scale all images to before overlaying them (format: width,height)
```

### TO-BLUE-CHANNEL-IS
Writes image segmentation files in the blue-channel format

#### Domain(s):
- **Image Segmentation Domain**

#### Options:
```
usage: to-blue-channel-is [--annotations-only] -o PATH [--split-names SPLIT NAME [SPLIT NAME ...]] [--split-ratios RATIO [RATIO ...]]

optional arguments:
  --annotations-only    skip the writing of data files, outputting only the annotation files
  -o PATH, --output PATH
                        the directory to write the annotation images to
  --split-names SPLIT NAME [SPLIT NAME ...]
                        the names to use for the splits
  --split-ratios RATIO [RATIO ...]
                        the ratios to use for the splits
```

### TO-COCO-OD
Writes image object-detection annotations in the MS-COCO JSON-format

#### Domain(s):
- **Image Object-Detection Domain**

#### Options:
```
usage: to-coco-od [--annotations-only] [--categories CATEGORY [CATEGORY ...]] [--category-output-file FILENAME] [--default-supercategory SUPERCATEGORY] [--error-on-new-category] [--license-name LICENSE_NAME] [--license-url LICENSE_URL] -o PATH [--pretty] [--sort-categories] [--split-names SPLIT NAME [SPLIT NAME ...]] [--split-ratios RATIO [RATIO ...]]

optional arguments:
  --annotations-only    skip the writing of data files, outputting only the annotation files
  --categories CATEGORY [CATEGORY ...]
                        defines the order of the categories
  --category-output-file FILENAME
                        file to write the categories into, as a simple comma-separated list
  --default-supercategory SUPERCATEGORY
                        the supercategory to use for pre-defined categories
  --error-on-new-category
                        whether unspecified categories should raise an error
  --license-name LICENSE_NAME
                        the license of the images
  --license-url LICENSE_URL
                        the license of the images
  -o PATH, --output PATH
                        output file to write annotations to (images are placed in same directory)
  --pretty              whether to format the JSON annotations file with indentation
  --sort-categories     whether to put the categories in alphabetical order
  --split-names SPLIT NAME [SPLIT NAME ...]
                        the names to use for the splits
  --split-ratios RATIO [RATIO ...]
                        the ratios to use for the splits
```

### TO-COMMON-VOICE-SP
Writes speech transcriptions in the Mozilla Common-Voice TSV-format

#### Domain(s):
- **Speech Domain**

#### Options:
```
usage: to-common-voice-sp [--annotations-only] -o PATH [--split-names SPLIT NAME [SPLIT NAME ...]] [--split-ratios RATIO [RATIO ...]]

optional arguments:
  --annotations-only    skip the writing of data files, outputting only the annotation files
  -o PATH, --output PATH
                        the filename of the TSV file to write the annotations into
  --split-names SPLIT NAME [SPLIT NAME ...]
                        the names to use for the splits
  --split-ratios RATIO [RATIO ...]
                        the ratios to use for the splits
```

### TO-FESTVOX-SP
Writes speech transcriptions in the Festival FestVox format

#### Domain(s):
- **Speech Domain**

#### Options:
```
usage: to-festvox-sp [--annotations-only] -o PATH [--split-names SPLIT NAME [SPLIT NAME ...]] [--split-ratios RATIO [RATIO ...]]

optional arguments:
  --annotations-only    skip the writing of data files, outputting only the annotation files
  -o PATH, --output PATH
                        the filename of the FestVox file to write the annotations into
  --split-names SPLIT NAME [SPLIT NAME ...]
                        the names to use for the splits
  --split-ratios RATIO [RATIO ...]
                        the ratios to use for the splits
```

### TO-INDEXED-PNG-IS
Writes image segmentation files in the indexed-PNG format

#### Domain(s):
- **Image Segmentation Domain**

#### Options:
```
usage: to-indexed-png-is [--annotations-only] -o PATH [--split-names SPLIT NAME [SPLIT NAME ...]] [--split-ratios RATIO [RATIO ...]]

optional arguments:
  --annotations-only    skip the writing of data files, outputting only the annotation files
  -o PATH, --output PATH
                        the directory to write the annotation images to
  --split-names SPLIT NAME [SPLIT NAME ...]
                        the names to use for the splits
  --split-ratios RATIO [RATIO ...]
                        the ratios to use for the splits
```

### TO-LAYER-SEGMENTS-IS
Writes the layer-segments image-segmentation format to disk

#### Domain(s):
- **Image Segmentation Domain**

#### Options:
```
usage: to-layer-segments-is [--annotations-only] [--label-separator SEPARATOR] -o PATH [--split-names SPLIT NAME [SPLIT NAME ...]] [--split-ratios RATIO [RATIO ...]]

optional arguments:
  --annotations-only    skip the writing of data files, outputting only the annotation files
  --label-separator SEPARATOR
                        the separator between the base filename and the label
  -o PATH, --output PATH
                        the directory to write the annotation images to
  --split-names SPLIT NAME [SPLIT NAME ...]
                        the names to use for the splits
  --split-ratios RATIO [RATIO ...]
                        the ratios to use for the splits
```

### TO-ROI-OD
Writes image object-detection annotations in the ROI CSV-format

#### Domain(s):
- **Image Object-Detection Domain**

#### Options:
```
usage: to-roi-od [-d WIDTH HEIGHT] [--annotations-only] [--comments COMMENTS [COMMENTS ...]] -o PATH [--size-mode] [--split-names SPLIT NAME [SPLIT NAME ...]] [--split-ratios RATIO [RATIO ...]] [--prefix WRITER_PREFIX] [--suffix WRITER_SUFFIX]

optional arguments:
  -d WIDTH HEIGHT, --image-dimensions WIDTH HEIGHT
                        image dimensions to use if none can be inferred
  --annotations-only    skip the writing of data files, outputting only the annotation files
  --comments COMMENTS [COMMENTS ...]
                        comments to write to the beginning of the ROI file
  -o PATH, --output PATH
                        output directory to write files to
  --size-mode           writes the ROI files with x,y,w,h headers instead of x0,y0,x1,y1
  --split-names SPLIT NAME [SPLIT NAME ...]
                        the names to use for the splits
  --split-ratios RATIO [RATIO ...]
                        the ratios to use for the splits
  --prefix WRITER_PREFIX
                        the prefix for output filenames (default = '')
  --suffix WRITER_SUFFIX
                        the suffix for output filenames (default = '-rois.csv')
```

### TO-SUBDIR-IC
Writes images to sub-directories named after their class labels.

#### Domain(s):
- **Image Classification Domain**

#### Options:
```
usage: to-subdir-ic -o PATH [--split-names SPLIT NAME [SPLIT NAME ...]] [--split-ratios RATIO [RATIO ...]]

optional arguments:
  -o PATH, --output PATH
                        the directory to store the class directories in
  --split-names SPLIT NAME [SPLIT NAME ...]
                        the names to use for the splits
  --split-ratios RATIO [RATIO ...]
                        the ratios to use for the splits
```

### TO-TF-OD
Writes image object-detection annotations in the TFRecords binary format

#### Domain(s):
- **Image Object-Detection Domain**

#### Options:
```
usage: to-tf-od [--dense] [--source-id-type {filename,numeric-dummy}] -o PATH [-p FILENAME] [-s FILENAME [FILENAME ...]] [--split-names SPLIT NAME [SPLIT NAME ...]] [--split-ratios RATIO [RATIO ...]]

optional arguments:
  --dense               outputs masks in the dense numerical format instead of PNG-encoded
  --source-id-type {filename,numeric-dummy}
                        by default, the filename gets stored in the 'source_id' field, but some algorithms try to convert it into a number and fail with 'StringToNumberOp could not correctly convert string'; in which case you can use 'numeric-dummy' (see https://github.com/google/automl/issues/307)
  -o PATH, --output PATH
                        name of output file for TFRecords
  -p FILENAME, --protobuf FILENAME
                        for storing the label strings and IDs
  -s FILENAME [FILENAME ...], --shards FILENAME [FILENAME ...]
                        additional shards to write to
  --split-names SPLIT NAME [SPLIT NAME ...]
                        the names to use for the splits
  --split-ratios RATIO [RATIO ...]
                        the ratios to use for the splits
```

### TO-VGG-OD
Writes image object-detection annotations in the VGG JSON-format

#### Domain(s):
- **Image Object-Detection Domain**

#### Options:
```
usage: to-vgg-od [--annotations-only] -o PATH [--pretty] [--split-names SPLIT NAME [SPLIT NAME ...]] [--split-ratios RATIO [RATIO ...]]

optional arguments:
  --annotations-only    skip the writing of data files, outputting only the annotation files
  -o PATH, --output PATH
                        output file to write annotations to (images are placed in same directory)
  --pretty              whether to format the JSON annotations file with indentation
  --split-names SPLIT NAME [SPLIT NAME ...]
                        the names to use for the splits
  --split-ratios RATIO [RATIO ...]
                        the ratios to use for the splits
```

### TO-VIDEO-FILE-OD
Writes frames to a MJPG video file.

#### Domain(s):
- **Image Object-Detection Domain**

#### Options:
```
usage: to-video-file-od [-f FPS] [-o OUTPUT_FILE]

optional arguments:
  -f FPS, --fps FPS     the frames per second to use
  -o OUTPUT_FILE, --output OUTPUT_FILE
                        the MJPG video file to write to
```

### TO-VOC-OD
Writes image object-detection annotations in the Pascal VOC XML-format

#### Domain(s):
- **Image Object-Detection Domain**

#### Options:
```
usage: to-voc-od [--annotations-only] -o PATH [--split-names SPLIT NAME [SPLIT NAME ...]] [--split-ratios RATIO [RATIO ...]]

optional arguments:
  --annotations-only    skip the writing of data files, outputting only the annotation files
  -o PATH, --output PATH
                        output directory to write annotations to (images are placed in same directory)
  --split-names SPLIT NAME [SPLIT NAME ...]
                        the names to use for the splits
  --split-ratios RATIO [RATIO ...]
                        the ratios to use for the splits
```

### TO-VOID-IC
Consumes instances without writing them.

#### Domain(s):
- **Image Classification Domain**

#### Options:
```
usage: to-void-ic
```

### TO-VOID-IS
Consumes instances without writing them.

#### Domain(s):
- **Image Segmentation Domain**

#### Options:
```
usage: to-void-is
```

### TO-VOID-OD
Consumes instances without writing them.

#### Domain(s):
- **Image Object-Detection Domain**

#### Options:
```
usage: to-void-od
```

### TO-VOID-SP
Consumes instances without writing them.

#### Domain(s):
- **Speech Domain**

#### Options:
```
usage: to-void-sp
```

### TO-YOLO-OD
Writes image object-detection annotations in the YOLO format

#### Domain(s):
- **Image Object-Detection Domain**

#### Options:
```
usage: to-yolo-od [-c PATH] [-l PATH] [--annotations-only] -o PATH [--split-names SPLIT NAME [SPLIT NAME ...]] [--split-ratios RATIO [RATIO ...]]

optional arguments:
  -c PATH, --labels-csv PATH
                        Path to the labels CSV file to write
  -l PATH, --labels PATH
                        Path to the labels file to write
  --annotations-only    skip the writing of data files, outputting only the annotation files
  -o PATH, --output PATH
                        output directory to write images and annotations to
  --split-names SPLIT NAME [SPLIT NAME ...]
                        the names to use for the splits
  --split-ratios RATIO [RATIO ...]
                        the ratios to use for the splits
```
