# Plugins
## Source stage
### FROM-ADAMS-IC
Reads image classification annotations in the ADAMS report-format

#### Domain(s):
- **Image Classification Domain**

#### Options:
```
usage: from-adams-ic [-I FILENAME] [-i FILENAME] [-N FILENAME] [-n FILENAME] [-o FILENAME]
                     [--seed SEED] [-e FORMAT FORMAT FORMAT] -c FIELD

optional arguments:
  -I FILENAME, --inputs-file FILENAME
                        Files containing lists of input files (can use glob syntax) (default: [])
  -i FILENAME, --input FILENAME
                        Input files (can use glob syntax) (default: [])
  -N FILENAME, --negatives-file FILENAME
                        Files containing lists of negative files (can use glob syntax) (default: [])
  -n FILENAME, --negative FILENAME
                        Files that have no annotations (can use glob syntax) (default: [])
  -o FILENAME, --output-file FILENAME
                        optional file to write read filenames into (default: None)
  --seed SEED           the seed to use for randomisation (default: None)
  -e FORMAT FORMAT FORMAT, --extensions FORMAT FORMAT FORMAT
                        image format extensions in order of preference (default: [<ImageFormat.PNG:
                        (frozenset({'png', 'PNG'}), 'PNG')>, <ImageFormat.JPG: (frozenset({'jpeg',
                        'JPG', 'JPEG', 'jpg'}), 'JPEG')>, <ImageFormat.BMP: (frozenset({'bmp',
                        'BMP'}), 'BMP')>])
  -c FIELD, --class-field FIELD
                        the report field containing the image class (default: None)
```

### FROM-ADAMS-OD
Reads image object-detection annotations in the ADAMS report-format

#### Domain(s):
- **Image Object-Detection Domain**

#### Options:
```
usage: from-adams-od [-I FILENAME] [-i FILENAME] [-N FILENAME] [-n FILENAME] [-o FILENAME]
                     [--seed SEED] [-e FORMAT FORMAT FORMAT] [-p PREFIXES [PREFIXES ...]]

optional arguments:
  -I FILENAME, --inputs-file FILENAME
                        Files containing lists of input files (can use glob syntax) (default: [])
  -i FILENAME, --input FILENAME
                        Input files (can use glob syntax) (default: [])
  -N FILENAME, --negatives-file FILENAME
                        Files containing lists of negative files (can use glob syntax) (default: [])
  -n FILENAME, --negative FILENAME
                        Files that have no annotations (can use glob syntax) (default: [])
  -o FILENAME, --output-file FILENAME
                        optional file to write read filenames into (default: None)
  --seed SEED           the seed to use for randomisation (default: None)
  -e FORMAT FORMAT FORMAT, --extensions FORMAT FORMAT FORMAT
                        image format extensions in order of preference (default: [<ImageFormat.PNG:
                        (frozenset({'png', 'PNG'}), 'PNG')>, <ImageFormat.JPG: (frozenset({'jpeg',
                        'JPG', 'JPEG', 'jpg'}), 'JPEG')>, <ImageFormat.BMP: (frozenset({'bmp',
                        'BMP'}), 'BMP')>])
  -p PREFIXES [PREFIXES ...], --prefixes PREFIXES [PREFIXES ...]
                        prefixes to parse (default: [])
```

### FROM-BLUE-CHANNEL-IS
Reads image segmentation files in the blue-channel format

#### Domain(s):
- **Image Segmentation Domain**

#### Options:
```
usage: from-blue-channel-is [-I FILENAME] [-i FILENAME] [-N FILENAME] [-n FILENAME] [-o FILENAME]
                            [--seed SEED] [--image-path-rel PATH] --labels LABEL [LABEL ...]

optional arguments:
  -I FILENAME, --inputs-file FILENAME
                        Files containing lists of input files (can use glob syntax) (default: [])
  -i FILENAME, --input FILENAME
                        Input files (can use glob syntax) (default: [])
  -N FILENAME, --negatives-file FILENAME
                        Files containing lists of negative files (can use glob syntax) (default: [])
  -n FILENAME, --negative FILENAME
                        Files that have no annotations (can use glob syntax) (default: [])
  -o FILENAME, --output-file FILENAME
                        optional file to write read filenames into (default: None)
  --seed SEED           the seed to use for randomisation (default: None)
  --image-path-rel PATH
                        Relative path to image files from annotations (default: .)
  --labels LABEL [LABEL ...]
                        specifies the labels for each index (default: None)
```

### FROM-COCO-OD
Reads image object-detection annotations in the MS-COCO JSON-format

#### Domain(s):
- **Image Object-Detection Domain**

#### Options:
```
usage: from-coco-od [-I FILENAME] [-i FILENAME] [-N FILENAME] [-n FILENAME] [-o FILENAME]
                    [--seed SEED]

optional arguments:
  -I FILENAME, --inputs-file FILENAME
                        Files containing lists of input files (can use glob syntax) (default: [])
  -i FILENAME, --input FILENAME
                        Input files (can use glob syntax) (default: [])
  -N FILENAME, --negatives-file FILENAME
                        Files containing lists of negative files (can use glob syntax) (default: [])
  -n FILENAME, --negative FILENAME
                        Files that have no annotations (can use glob syntax) (default: [])
  -o FILENAME, --output-file FILENAME
                        optional file to write read filenames into (default: None)
  --seed SEED           the seed to use for randomisation (default: None)
```

### FROM-COMMON-VOICE-SP
Reads speech transcriptions in the Mozilla Common-Voice TSV-format

#### Domain(s):
- **Speech Domain**

#### Options:
```
usage: from-common-voice-sp [-I FILENAME] [-i FILENAME] [-N FILENAME] [-n FILENAME] [-o FILENAME]
                            [--seed SEED] [--rel-path REL_PATH]

optional arguments:
  -I FILENAME, --inputs-file FILENAME
                        Files containing lists of input files (can use glob syntax) (default: [])
  -i FILENAME, --input FILENAME
                        Input files (can use glob syntax) (default: [])
  -N FILENAME, --negatives-file FILENAME
                        Files containing lists of negative files (can use glob syntax) (default: [])
  -n FILENAME, --negative FILENAME
                        Files that have no annotations (can use glob syntax) (default: [])
  -o FILENAME, --output-file FILENAME
                        optional file to write read filenames into (default: None)
  --seed SEED           the seed to use for randomisation (default: None)
  --rel-path REL_PATH   the relative path from the annotations file to the audio files (default: .)
```

### FROM-FESTVOX-SP
Reads speech transcriptions in the Festival FestVox format

#### Domain(s):
- **Speech Domain**

#### Options:
```
usage: from-festvox-sp [-I FILENAME] [-i FILENAME] [-N FILENAME] [-n FILENAME] [-o FILENAME]
                       [--seed SEED] [--rel-path REL_PATH]

optional arguments:
  -I FILENAME, --inputs-file FILENAME
                        Files containing lists of input files (can use glob syntax) (default: [])
  -i FILENAME, --input FILENAME
                        Input files (can use glob syntax) (default: [])
  -N FILENAME, --negatives-file FILENAME
                        Files containing lists of negative files (can use glob syntax) (default: [])
  -n FILENAME, --negative FILENAME
                        Files that have no annotations (can use glob syntax) (default: [])
  -o FILENAME, --output-file FILENAME
                        optional file to write read filenames into (default: None)
  --seed SEED           the seed to use for randomisation (default: None)
  --rel-path REL_PATH   the relative path from the annotations file to the audio files (default: .)
```

### FROM-GRAYSCALE-IS
Reads image segmentation files in the grayscale format

#### Domain(s):
- **Image Segmentation Domain**

#### Options:
```
usage: from-grayscale-is [-I FILENAME] [-i FILENAME] [-N FILENAME] [-n FILENAME] [-o FILENAME]
                         [--seed SEED] [--image-path-rel PATH] --labels LABEL [LABEL ...]

optional arguments:
  -I FILENAME, --inputs-file FILENAME
                        Files containing lists of input files (can use glob syntax) (default: [])
  -i FILENAME, --input FILENAME
                        Input files (can use glob syntax) (default: [])
  -N FILENAME, --negatives-file FILENAME
                        Files containing lists of negative files (can use glob syntax) (default: [])
  -n FILENAME, --negative FILENAME
                        Files that have no annotations (can use glob syntax) (default: [])
  -o FILENAME, --output-file FILENAME
                        optional file to write read filenames into (default: None)
  --seed SEED           the seed to use for randomisation (default: None)
  --image-path-rel PATH
                        Relative path to image files from annotations (default: .)
  --labels LABEL [LABEL ...]
                        specifies the labels for each index (default: None)
```

### FROM-IMAGES-IC
Dummy reader that turns images into an image classification dataset.

#### Domain(s):
- **Image Classification Domain**

#### Options:
```
usage: from-images-ic [-I FILENAME] [-i FILENAME] [-N FILENAME] [-n FILENAME] [-o FILENAME]
                      [--seed SEED]

optional arguments:
  -I FILENAME, --inputs-file FILENAME
                        Files containing lists of input files (can use glob syntax) (default: [])
  -i FILENAME, --input FILENAME
                        Input files (can use glob syntax) (default: [])
  -N FILENAME, --negatives-file FILENAME
                        Files containing lists of negative files (can use glob syntax) (default: [])
  -n FILENAME, --negative FILENAME
                        Files that have no annotations (can use glob syntax) (default: [])
  -o FILENAME, --output-file FILENAME
                        optional file to write read filenames into (default: None)
  --seed SEED           the seed to use for randomisation (default: None)
```

### FROM-IMAGES-IS
Dummy reader that turns images into an image segmentation dataset.

#### Domain(s):
- **Image Segmentation Domain**

#### Options:
```
usage: from-images-is [-I FILENAME] [-i FILENAME] [-N FILENAME] [-n FILENAME] [-o FILENAME]
                      [--seed SEED]

optional arguments:
  -I FILENAME, --inputs-file FILENAME
                        Files containing lists of input files (can use glob syntax) (default: [])
  -i FILENAME, --input FILENAME
                        Input files (can use glob syntax) (default: [])
  -N FILENAME, --negatives-file FILENAME
                        Files containing lists of negative files (can use glob syntax) (default: [])
  -n FILENAME, --negative FILENAME
                        Files that have no annotations (can use glob syntax) (default: [])
  -o FILENAME, --output-file FILENAME
                        optional file to write read filenames into (default: None)
  --seed SEED           the seed to use for randomisation (default: None)
```

### FROM-IMAGES-OD
Dummy reader that turns images into an object detection dataset.

#### Domain(s):
- **Image Object-Detection Domain**

#### Options:
```
usage: from-images-od [-I FILENAME] [-i FILENAME] [-N FILENAME] [-n FILENAME] [-o FILENAME]
                      [--seed SEED]

optional arguments:
  -I FILENAME, --inputs-file FILENAME
                        Files containing lists of input files (can use glob syntax) (default: [])
  -i FILENAME, --input FILENAME
                        Input files (can use glob syntax) (default: [])
  -N FILENAME, --negatives-file FILENAME
                        Files containing lists of negative files (can use glob syntax) (default: [])
  -n FILENAME, --negative FILENAME
                        Files that have no annotations (can use glob syntax) (default: [])
  -o FILENAME, --output-file FILENAME
                        optional file to write read filenames into (default: None)
  --seed SEED           the seed to use for randomisation (default: None)
```

### FROM-INDEXED-PNG-IS
Reads image segmentation files in the indexed-PNG format

#### Domain(s):
- **Image Segmentation Domain**

#### Options:
```
usage: from-indexed-png-is [-I FILENAME] [-i FILENAME] [-N FILENAME] [-n FILENAME] [-o FILENAME]
                           [--seed SEED] [--image-path-rel PATH] --labels LABEL [LABEL ...]

optional arguments:
  -I FILENAME, --inputs-file FILENAME
                        Files containing lists of input files (can use glob syntax) (default: [])
  -i FILENAME, --input FILENAME
                        Input files (can use glob syntax) (default: [])
  -N FILENAME, --negatives-file FILENAME
                        Files containing lists of negative files (can use glob syntax) (default: [])
  -n FILENAME, --negative FILENAME
                        Files that have no annotations (can use glob syntax) (default: [])
  -o FILENAME, --output-file FILENAME
                        optional file to write read filenames into (default: None)
  --seed SEED           the seed to use for randomisation (default: None)
  --image-path-rel PATH
                        Relative path to image files from annotations (default: .)
  --labels LABEL [LABEL ...]
                        specifies the labels for each index (default: None)
```

### FROM-LAYER-SEGMENTS-IS
Reads in the layer-segments image-segmentation format from disk, where each label has a binary PNG storing the mask for that label

#### Domain(s):
- **Image Segmentation Domain**

#### Options:
```
usage: from-layer-segments-is [-I FILENAME] [-i FILENAME] [-N FILENAME] [-n FILENAME] [-o FILENAME]
                              [--seed SEED] [--label-separator SEPARATOR] --labels LABEL [LABEL ...]
                              [--image-path-rel PATH]

optional arguments:
  -I FILENAME, --inputs-file FILENAME
                        Files containing lists of input files (can use glob syntax) (default: [])
  -i FILENAME, --input FILENAME
                        Input files (can use glob syntax) (default: [])
  -N FILENAME, --negatives-file FILENAME
                        Files containing lists of negative files (can use glob syntax) (default: [])
  -n FILENAME, --negative FILENAME
                        Files that have no annotations (can use glob syntax) (default: [])
  -o FILENAME, --output-file FILENAME
                        optional file to write read filenames into (default: None)
  --seed SEED           the seed to use for randomisation (default: None)
  --label-separator SEPARATOR
                        the separator between the base filename and the label (default: -)
  --labels LABEL [LABEL ...]
                        specifies the labels for each index (default: None)
  --image-path-rel PATH
                        Relative path to image files from annotations (default: .)
```

### FROM-OPEX-OD
Reads image object-detection annotations in the OPEX format

#### Domain(s):
- **Image Object-Detection Domain**

#### Options:
```
usage: from-opex-od [-I FILENAME] [-i FILENAME] [-N FILENAME] [-n FILENAME] [-o FILENAME]
                    [--seed SEED]

optional arguments:
  -I FILENAME, --inputs-file FILENAME
                        Files containing lists of input files (can use glob syntax) (default: [])
  -i FILENAME, --input FILENAME
                        Input files (can use glob syntax) (default: [])
  -N FILENAME, --negatives-file FILENAME
                        Files containing lists of negative files (can use glob syntax) (default: [])
  -n FILENAME, --negative FILENAME
                        Files that have no annotations (can use glob syntax) (default: [])
  -o FILENAME, --output-file FILENAME
                        optional file to write read filenames into (default: None)
  --seed SEED           the seed to use for randomisation (default: None)
```

### FROM-ROI-OD
Reads image object-detection annotations in the ROI CSV-format

#### Domain(s):
- **Image Object-Detection Domain**

#### Options:
```
usage: from-roi-od [-I FILENAME] [-i FILENAME] [-N FILENAME] [-n FILENAME] [-o FILENAME]
                   [--seed SEED] [-e FORMAT FORMAT FORMAT] [--prefix READER_PREFIX]
                   [--suffix READER_SUFFIX]

optional arguments:
  -I FILENAME, --inputs-file FILENAME
                        Files containing lists of input files (can use glob syntax) (default: [])
  -i FILENAME, --input FILENAME
                        Input files (can use glob syntax) (default: [])
  -N FILENAME, --negatives-file FILENAME
                        Files containing lists of negative files (can use glob syntax) (default: [])
  -n FILENAME, --negative FILENAME
                        Files that have no annotations (can use glob syntax) (default: [])
  -o FILENAME, --output-file FILENAME
                        optional file to write read filenames into (default: None)
  --seed SEED           the seed to use for randomisation (default: None)
  -e FORMAT FORMAT FORMAT, --extensions FORMAT FORMAT FORMAT
                        image format extensions in order of preference (default: [<ImageFormat.PNG:
                        (frozenset({'png', 'PNG'}), 'PNG')>, <ImageFormat.JPG: (frozenset({'jpeg',
                        'JPG', 'JPEG', 'jpg'}), 'JPEG')>, <ImageFormat.BMP: (frozenset({'bmp',
                        'BMP'}), 'BMP')>])
  --prefix READER_PREFIX
                        the prefix for output filenames (default = '') (default: None)
  --suffix READER_SUFFIX
                        the suffix for output filenames (default = '-rois.csv') (default: None)
```

### FROM-SUBDIR-IC
Reads images from sub-directories named after their class labels.

#### Domain(s):
- **Image Classification Domain**

#### Options:
```
usage: from-subdir-ic [-I FILENAME] [-i FILENAME] [-N FILENAME] [-n FILENAME] [-o FILENAME]
                      [--seed SEED]

optional arguments:
  -I FILENAME, --inputs-file FILENAME
                        Files containing lists of input files (can use glob syntax) (default: [])
  -i FILENAME, --input FILENAME
                        Input files (can use glob syntax) (default: [])
  -N FILENAME, --negatives-file FILENAME
                        Files containing lists of negative files (can use glob syntax) (default: [])
  -n FILENAME, --negative FILENAME
                        Files that have no annotations (can use glob syntax) (default: [])
  -o FILENAME, --output-file FILENAME
                        optional file to write read filenames into (default: None)
  --seed SEED           the seed to use for randomisation (default: None)
```

### FROM-TF-OD
Reads image object-detection annotations in the TFRecords binary format

#### Domain(s):
- **Image Object-Detection Domain**

#### Options:
```
usage: from-tf-od [-I FILENAME] [-i FILENAME] [-N FILENAME] [-n FILENAME] [-o FILENAME]
                  [--seed SEED] [--mask-threshold THRESHOLD] [--sample-stride STRIDE]

optional arguments:
  -I FILENAME, --inputs-file FILENAME
                        Files containing lists of input files (can use glob syntax) (default: [])
  -i FILENAME, --input FILENAME
                        Input files (can use glob syntax) (default: [])
  -N FILENAME, --negatives-file FILENAME
                        Files containing lists of negative files (can use glob syntax) (default: [])
  -n FILENAME, --negative FILENAME
                        Files that have no annotations (can use glob syntax) (default: [])
  -o FILENAME, --output-file FILENAME
                        optional file to write read filenames into (default: None)
  --seed SEED           the seed to use for randomisation (default: None)
  --mask-threshold THRESHOLD
                        the threshold to use when calculating polygons from masks (default: 0.9)
  --sample-stride STRIDE
                        the stride to use when calculating polygons from masks (default: 1)
```

### FROM-VGG-OD
Reads image object-detection annotations in the VGG JSON-format

#### Domain(s):
- **Image Object-Detection Domain**

#### Options:
```
usage: from-vgg-od [-I FILENAME] [-i FILENAME] [-N FILENAME] [-n FILENAME] [-o FILENAME]
                   [--seed SEED]

optional arguments:
  -I FILENAME, --inputs-file FILENAME
                        Files containing lists of input files (can use glob syntax) (default: [])
  -i FILENAME, --input FILENAME
                        Input files (can use glob syntax) (default: [])
  -N FILENAME, --negatives-file FILENAME
                        Files containing lists of negative files (can use glob syntax) (default: [])
  -n FILENAME, --negative FILENAME
                        Files that have no annotations (can use glob syntax) (default: [])
  -o FILENAME, --output-file FILENAME
                        optional file to write read filenames into (default: None)
  --seed SEED           the seed to use for randomisation (default: None)
```

### FROM-VIDEO-FILE-OD
Reads frames from a video file.

#### Domain(s):
- **Image Object-Detection Domain**

#### Options:
```
usage: from-video-file-od [-f FROM_FRAME] [-i INPUT_FILE] [-m MAX_FRAMES] [-n NTH_FRAME] [-p PREFIX]
                          [-t TO_FRAME]

optional arguments:
  -f FROM_FRAME, --from-frame FROM_FRAME
                        determines with which frame to start the stream (1-based index) (default: 1)
  -i INPUT_FILE, --input INPUT_FILE
                        the video file to read (default: )
  -m MAX_FRAMES, --max-frames MAX_FRAMES
                        determines the maximum number of frames to read; ignored if <=0 (default:
                        -1)
  -n NTH_FRAME, --nth-frame NTH_FRAME
                        determines whether frames get skipped and only evert nth frame gets
                        forwarded (default: 1)
  -p PREFIX, --prefix PREFIX
                        the prefix to use for the frames (default: )
  -t TO_FRAME, --to-frame TO_FRAME
                        determines after which frame to stop (1-based index); ignored if <=0
                        (default: -1)
```

### FROM-VOC-OD
Reads image object-detection annotations in the Pascal VOC XML-format

#### Domain(s):
- **Image Object-Detection Domain**

#### Options:
```
usage: from-voc-od [-I FILENAME] [-i FILENAME] [-N FILENAME] [-n FILENAME] [-o FILENAME]
                   [--seed SEED]

optional arguments:
  -I FILENAME, --inputs-file FILENAME
                        Files containing lists of input files (can use glob syntax) (default: [])
  -i FILENAME, --input FILENAME
                        Input files (can use glob syntax) (default: [])
  -N FILENAME, --negatives-file FILENAME
                        Files containing lists of negative files (can use glob syntax) (default: [])
  -n FILENAME, --negative FILENAME
                        Files that have no annotations (can use glob syntax) (default: [])
  -o FILENAME, --output-file FILENAME
                        optional file to write read filenames into (default: None)
  --seed SEED           the seed to use for randomisation (default: None)
```

### FROM-WEBCAM-OD
Reads frames from a webcam.

#### Domain(s):
- **Image Object-Detection Domain**

#### Options:
```
usage: from-webcam-od [-f FROM_FRAME] [-m MAX_FRAMES] [-n NTH_FRAME] [-p PREFIX] [-t TO_FRAME]
                      [-i WEBCAM_ID]

optional arguments:
  -f FROM_FRAME, --from-frame FROM_FRAME
                        determines with which frame to start the stream (1-based index) (default: 1)
  -m MAX_FRAMES, --max-frames MAX_FRAMES
                        determines the maximum number of frames to read; ignored if <=0 (default:
                        -1)
  -n NTH_FRAME, --nth-frame NTH_FRAME
                        determines whether frames get skipped and only evert nth frame gets
                        forwarded (default: 1)
  -p PREFIX, --prefix PREFIX
                        the prefix to use for the frames (default: webcam-)
  -t TO_FRAME, --to-frame TO_FRAME
                        determines after which frame to stop (1-based index); ignored if <=0
                        (default: -1)
  -i WEBCAM_ID, --webcam-id WEBCAM_ID
                        the webcam ID to read from (default: 0)
```

### FROM-YOLO-OD
Reads image object-detection annotations in the YOLO format

#### Domain(s):
- **Image Object-Detection Domain**

#### Options:
```
usage: from-yolo-od [-I FILENAME] [-i FILENAME] [-N FILENAME] [-n FILENAME] [-o FILENAME]
                    [--seed SEED] [--image-path-rel PATH] [-l PATH]

optional arguments:
  -I FILENAME, --inputs-file FILENAME
                        Files containing lists of input files (can use glob syntax) (default: [])
  -i FILENAME, --input FILENAME
                        Input files (can use glob syntax) (default: [])
  -N FILENAME, --negatives-file FILENAME
                        Files containing lists of negative files (can use glob syntax) (default: [])
  -n FILENAME, --negative FILENAME
                        Files that have no annotations (can use glob syntax) (default: [])
  -o FILENAME, --output-file FILENAME
                        optional file to write read filenames into (default: None)
  --seed SEED           the seed to use for randomisation (default: None)
  --image-path-rel PATH
                        Relative path to image files from annotations (default: None)
  -l PATH, --labels PATH
                        Path to the labels file (default: None)
```


## Processor stage
### ADD-ANNOTATION-OVERLAY-IC
Adds the image classification label on top of images passing through.

#### Domain(s):
- **Image Classification Domain**

#### Options:
```
usage: add-annotation-overlay-ic [--background-color BACKGROUND_COLOR]
                                 [--background-margin BACKGROUND_MARGIN] [--fill-background]
                                 [--font-color FONT_COLOR] [--font-family FONT_FAMILY]
                                 [--font-size FONT_SIZE] [--position TEXT_PLACEMENT]

optional arguments:
  --background-color BACKGROUND_COLOR
                        the RGB color triplet to use for the background. (default: 0,0,0)
  --background-margin BACKGROUND_MARGIN
                        the margin in pixels around the background. (default: 2)
  --fill-background     whether to fill the background of the text with the specified color.
                        (default: False)
  --font-color FONT_COLOR
                        the RGB color triplet to use for the font. (default: 255,255,255)
  --font-family FONT_FAMILY
                        the name of the TTF font-family to use, note: any hyphens need escaping with
                        backslash. (default: sans\-serif)
  --font-size FONT_SIZE
                        the size of the font. (default: 14)
  --position TEXT_PLACEMENT
                        the position of the label (X,Y). (default: 5,5)
```

### ADD-ANNOTATION-OVERLAY-IS
Adds the image segmentation annotations on top of images passing through.

#### Domain(s):
- **Image Segmentation Domain**

#### Options:
```
usage: add-annotation-overlay-is [--alpha ALPHA] [--colors COLORS [COLORS ...]]
                                 [--labels LABELS [LABELS ...]]

optional arguments:
  --alpha ALPHA         the alpha value to use for overlaying the annotations (0: transparent, 255:
                        opaque). (default: 64)
  --colors COLORS [COLORS ...]
                        the RGB triplets (R,G,B) of custom colors to use, uses default colors if not
                        supplied (default: [])
  --labels LABELS [LABELS ...]
                        the labels of annotations to overlay, overlays all if omitted (default: [])
```

### ADD-ANNOTATION-OVERLAY-OD
Adds object detection overlays to images passing through.

#### Domain(s):
- **Image Object-Detection Domain**

#### Options:
```
usage: add-annotation-overlay-od [--colors COLORS [COLORS ...]] [--fill] [--fill-alpha FILL_ALPHA]
                                 [--font-family FONT_FAMILY] [--font-size FONT_SIZE] [--force-bbox]
                                 [--label-key LABEL_KEY] [--labels LABELS [LABELS ...]]
                                 [--num-decimals NUM_DECIMALS] [--outline-alpha OUTLINE_ALPHA]
                                 [--outline-thickness OUTLINE_THICKNESS] [--text-format TEXT_FORMAT]
                                 [--text-placement TEXT_PLACEMENT] [--vary-colors]

optional arguments:
  --colors COLORS [COLORS ...]
                        the RGB triplets (R,G,B) of custom colors to use, uses default colors if not
                        supplied (default: [])
  --fill                whether to fill the bounding boxes/polygons (default: False)
  --fill-alpha FILL_ALPHA
                        the alpha value to use for the filling (0: transparent, 255: opaque).
                        (default: 128)
  --font-family FONT_FAMILY
                        the name of the TTF font-family to use, note: any hyphens need escaping with
                        backslash. (default: sans\-serif)
  --font-size FONT_SIZE
                        the size of the font. (default: 14)
  --force-bbox          whether to force a bounding box even if there is a polygon available
                        (default: False)
  --label-key LABEL_KEY
                        the key in the meta-data that contains the label. (default: type)
  --labels LABELS [LABELS ...]
                        the labels of annotations to overlay, overlays all if omitted (default: [])
  --num-decimals NUM_DECIMALS
                        the number of decimals to use for float numbers in the text format string.
                        (default: 3)
  --outline-alpha OUTLINE_ALPHA
                        the alpha value to use for the outline (0: transparent, 255: opaque).
                        (default: 255)
  --outline-thickness OUTLINE_THICKNESS
                        the line thickness to use for the outline, <1 to turn off. (default: 3)
  --text-format TEXT_FORMAT
                        template for the text to print on top of the bounding box or polygon, '{PH}'
                        is a placeholder for the 'PH' value from the meta-data or 'label' for the
                        current label; ignored if empty. (default: {label})
  --text-placement TEXT_PLACEMENT
                        comma-separated list of vertical (T=top, C=center, B=bottom) and horizontal
                        (L=left, C=center, R=right) anchoring. (default: T,L)
  --vary-colors         whether to vary the colors of the outline/filling regardless of label
                        (default: False)
```

### CHECK-DUPLICATE-FILENAMES
Causes the conversion stream to halt when multiple dataset items have the same filename

#### Domain(s):
- **Image Segmentation Domain**
- **Image Object-Detection Domain**
- **Speech Domain**
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

### COMBINE-ANNOTATIONS-OD
Combines object detection annotations from images passing through into a single annotation.

#### Domain(s):
- **Image Object-Detection Domain**

#### Options:
```
usage: combine-annotations-od [--combination COMBINATION] [--min-iou MIN_IOU]

optional arguments:
  --combination COMBINATION
                        how to combine the annotations (union|intersect); the 'stream_index' key in
                        the meta-data contains the stream index (default: intersect)
  --min-iou MIN_IOU     the minimum IoU (intersect over union) to use for identifying objects that
                        overlap (default: 0.7)
```

### CONVERT-IMAGE-FORMAT
Converts images from one format to another

#### Domain(s):
- **Image Segmentation Domain**
- **Image Object-Detection Domain**
- **Image Classification Domain**

#### Options:
```
usage: convert-image-format -f FORMAT

optional arguments:
  -f FORMAT, --format FORMAT
                        format to convert images to (default: None)
```

### CROP
Crops images.

#### Domain(s):
- **Image Object-Detection Domain**
- **Image Classification Domain**

#### Options:
```
usage: crop [-m IMGAUG_MODE] [--suffix IMGAUG_SUFFIX] [-f PERCENT_FROM] [-t PERCENT_TO] [-s SEED]
            [-a] [-T THRESHOLD] [-u]

optional arguments:
  -m IMGAUG_MODE, --mode IMGAUG_MODE
                        the image augmentation mode to use, available modes: replace, add (default:
                        replace)
  --suffix IMGAUG_SUFFIX
                        the suffix to use for the file names in case of augmentation mode add
                        (default: None)
  -f PERCENT_FROM, --from-percent PERCENT_FROM
                        the minimum percent to crop from images (default: None)
  -t PERCENT_TO, --to-percent PERCENT_TO
                        the maximum percent to crop from images (default: None)
  -s SEED, --seed SEED  the seed value to use for the random number generator; randomly seeded if
                        not provided (default: None)
  -a, --seed-augmentation
                        whether to seed the augmentation; if specified, uses the seeded random
                        generator to produce a seed value from 0 to 1000 for the augmentation.
                        (default: False)
  -T THRESHOLD, --threshold THRESHOLD
                        the threshold to use for Random.rand(): if equal or above, augmentation gets
                        applied; range: 0-1; default: 0 (= always) (default: None)
  -u, --update-size     whether to update the image size after the crop operation or scale back to
                        original size (default: False)
```

### DIMENSION-DISCARDER
Removes annotations which fall outside certain size constraints

#### Domain(s):
- **Image Object-Detection Domain**

#### Options:
```
usage: dimension-discarder [--max-area MAX_AREA] [--max-height MAX_HEIGHT] [--max-width MAX_WIDTH]
                           [--min-area MIN_AREA] [--min-height MIN_HEIGHT] [--min-width MIN_WIDTH]
                           [--verbose]

optional arguments:
  --max-area MAX_AREA   the maximum area of annotations to convert (default: None)
  --max-height MAX_HEIGHT
                        the maximum height of annotations to convert (default: None)
  --max-width MAX_WIDTH
                        the maximum width of annotations to convert (default: None)
  --min-area MIN_AREA   the minimum area of annotations to convert (default: None)
  --min-height MIN_HEIGHT
                        the minimum height of annotations to convert (default: None)
  --min-width MIN_WIDTH
                        the minimum width of annotations to convert (default: None)
  --verbose             outputs information when discarding annotations (default: False)
```

### DISCARD-INVALID-IMAGES
Discards images that cannot be loaded (e.g., corrupt image file or annotations with no image)

#### Domain(s):
- **Image Segmentation Domain**
- **Image Object-Detection Domain**
- **Image Classification Domain**

#### Options:
```
usage: discard-invalid-images [-v]

optional arguments:
  -v, --verbose  whether to output debugging information (default: False)
```

### DISCARD-NEGATIVES
Discards negative examples (those without annotations) from the stream

#### Domain(s):
- **Image Segmentation Domain**
- **Image Object-Detection Domain**
- **Speech Domain**
- **Image Classification Domain**

#### Options:
```
usage: discard-negatives
```

### DROP-FRAMES
Drops frames from the stream.

#### Domain(s):
- **Image Segmentation Domain**
- **Image Object-Detection Domain**
- **Image Classification Domain**

#### Options:
```
usage: drop-frames [-n NTH_FRAME]

optional arguments:
  -n NTH_FRAME, --nth-frame NTH_FRAME
                        which nth frame to drop, e..g, '2' means to drop every 2nd frame; passes
                        frames through if <=1 (default: 0)
```

### FILTER-FRAMES-BY-LABEL-OD
Filters frames from the stream using the labels in the annotations, i.e., keeps or drops frames depending on presence/absence of labels.

#### Domain(s):
- **Image Segmentation Domain**
- **Image Object-Detection Domain**
- **Image Classification Domain**

#### Options:
```
usage: filter-frames-by-label-od [--excluded-labels EXCLUDED_LABELS] [--key-label KEY_LABEL]
                                 [--key-score KEY_SCORE] [--min-score MIN_SCORE]
                                 [--required-labels REQUIRED_LABELS] [-v]

optional arguments:
  --excluded-labels EXCLUDED_LABELS
                        the comma-separated list of labels that will automatically drop the frame
                        when present in the frame (default: )
  --key-label KEY_LABEL
                        the meta-data key in the annotations that contains the label. (default:
                        type)
  --key-score KEY_SCORE
                        the meta-data key in the annotations to use for storing the prediction
                        score. (default: score)
  --min-score MIN_SCORE
                        the minimum score that predictions must have in order to be included in the
                        label checks, ignored if not supplied (default: None)
  --required-labels REQUIRED_LABELS
                        the comma-separated list of labels that must be present in the frame,
                        otherwise it gets dropped (default: )
  -v, --verbose         whether to output debugging information. (default: False)
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
                        labels to use (default: [])
  -r regexp, --regexp regexp
                        regular expression for using only a subset of labels (default: None)
```

### FILTER-METADATA
Filters detected objects based on their meta-data.

#### Domain(s):
- **Image Object-Detection Domain**

#### Options:
```
usage: filter-metadata [-c COMPARISON] [-k KEY] [-t VALUE_TYPE]

optional arguments:
  -c COMPARISON, --comparison COMPARISON
                        the comparison to apply to the value: for bool/numeric/string '=OTHER' and
                        '!=OTHER' can be used, for numeric furthermore '<OTHER', '<=OTHER',
                        '>=OTHER', '>OTHER'. E.g.: '<3.0' for numeric types will discard any
                        annotations that have a value of 3.0 or larger (default: None)
  -k KEY, --key KEY     the key of the meta-data value to use for the filtering (default: None)
  -t VALUE_TYPE, --value-type VALUE_TYPE
                        the data type that the value represents, available options:
                        bool|numeric|string (default: None)
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
                        the direction to flip, available options: lr, up, lrup (default: None)
  -m IMGAUG_MODE, --mode IMGAUG_MODE
                        the image augmentation mode to use, available modes: replace, add (default:
                        replace)
  --suffix IMGAUG_SUFFIX
                        the suffix to use for the file names in case of augmentation mode add
                        (default: None)
  -s SEED, --seed SEED  the seed value to use for the random number generator; randomly seeded if
                        not provided (default: None)
  -a, --seed-augmentation
                        whether to seed the augmentation; if specified, uses the seeded random
                        generator to produce a seed value from 0 to 1000 for the augmentation.
                        (default: False)
  -T THRESHOLD, --threshold THRESHOLD
                        the threshold to use for Random.rand(): if equal or above, augmentation gets
                        applied; range: 0-1; default: 0 (= always) (default: None)
```

### GAUSSIAN-BLUR
Applies gaussian blur to images.

#### Domain(s):
- **Image Object-Detection Domain**
- **Image Classification Domain**

#### Options:
```
usage: gaussian-blur [-m IMGAUG_MODE] [--suffix IMGAUG_SUFFIX] [-s SEED] [-a] [-f SIGMA_FROM]
                     [-t SIGMA_TO] [-T THRESHOLD]

optional arguments:
  -m IMGAUG_MODE, --mode IMGAUG_MODE
                        the image augmentation mode to use, available modes: replace, add (default:
                        replace)
  --suffix IMGAUG_SUFFIX
                        the suffix to use for the file names in case of augmentation mode add
                        (default: None)
  -s SEED, --seed SEED  the seed value to use for the random number generator; randomly seeded if
                        not provided (default: None)
  -a, --seed-augmentation
                        whether to seed the augmentation; if specified, uses the seeded random
                        generator to produce a seed value from 0 to 1000 for the augmentation.
                        (default: False)
  -f SIGMA_FROM, --from-sigma SIGMA_FROM
                        the minimum sigma for the blur to apply to the images (default: None)
  -t SIGMA_TO, --to-sigma SIGMA_TO
                        the maximum sigma for the blur to apply to the images (default: None)
  -T THRESHOLD, --threshold THRESHOLD
                        the threshold to use for Random.rand(): if equal or above, augmentation gets
                        applied; range: 0-1; default: 0 (= always) (default: None)
```

### HSL-GRAYSCALE
Turns RGB images into fake grayscale ones by converting them to HSL and then using the L channel for all channels. The brightness can be influenced and varied even.

#### Domain(s):
- **Image Object-Detection Domain**
- **Image Classification Domain**

#### Options:
```
usage: hsl-grayscale [-f FACTOR_FROM] [-t FACTOR_TO] [-m IMGAUG_MODE] [--suffix IMGAUG_SUFFIX]
                     [-s SEED] [-a] [-T THRESHOLD]

optional arguments:
  -f FACTOR_FROM, --from-factor FACTOR_FROM
                        the start of the factor range to apply to the L channel to darken or lighten
                        the image (<1: darker, >1: lighter) (default: None)
  -t FACTOR_TO, --to-factor FACTOR_TO
                        the end of the factor range to apply to the L channel to darken or lighten
                        the image (<1: darker, >1: lighter) (default: None)
  -m IMGAUG_MODE, --mode IMGAUG_MODE
                        the image augmentation mode to use, available modes: replace, add (default:
                        replace)
  --suffix IMGAUG_SUFFIX
                        the suffix to use for the file names in case of augmentation mode add
                        (default: None)
  -s SEED, --seed SEED  the seed value to use for the random number generator; randomly seeded if
                        not provided (default: None)
  -a, --seed-augmentation
                        whether to seed the augmentation; if specified, uses the seeded random
                        generator to produce a seed value from 0 to 1000 for the augmentation.
                        (default: False)
  -T THRESHOLD, --threshold THRESHOLD
                        the threshold to use for Random.rand(): if equal or above, augmentation gets
                        applied; range: 0-1; default: 0 (= always) (default: None)
```

### LINEAR-CONTRAST
Applies linear contrast to images.

#### Domain(s):
- **Image Object-Detection Domain**
- **Image Classification Domain**

#### Options:
```
usage: linear-contrast [-f ALPHA_FROM] [-t ALPHA_TO] [-m IMGAUG_MODE] [--suffix IMGAUG_SUFFIX]
                       [-s SEED] [-a] [-T THRESHOLD]

optional arguments:
  -f ALPHA_FROM, --from-alpha ALPHA_FROM
                        the minimum alpha to apply to the images (default: None)
  -t ALPHA_TO, --to-alpha ALPHA_TO
                        the maximum alpha to apply to the images (default: None)
  -m IMGAUG_MODE, --mode IMGAUG_MODE
                        the image augmentation mode to use, available modes: replace, add (default:
                        replace)
  --suffix IMGAUG_SUFFIX
                        the suffix to use for the file names in case of augmentation mode add
                        (default: None)
  -s SEED, --seed SEED  the seed value to use for the random number generator; randomly seeded if
                        not provided (default: None)
  -a, --seed-augmentation
                        whether to seed the augmentation; if specified, uses the seeded random
                        generator to produce a seed value from 0 to 1000 for the augmentation.
                        (default: False)
  -T THRESHOLD, --threshold THRESHOLD
                        the threshold to use for Random.rand(): if equal or above, augmentation gets
                        applied; range: 0-1; default: 0 (= always) (default: None)
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
                        mapping for labels, for replacing one label string with another (eg when
                        fixing/collapsing labels) (default: [])
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
                        how to handle instances with more than one located object (default: error)
```

### OD-TO-IS
Converts image object-detection instances into image segmentation instances

#### Domain(s):
- **Image Object-Detection Domain**

#### Options:
```
usage: od-to-is [--label-error] --labels LABEL [LABEL ...]

optional arguments:
  --label-error         whether to raise errors when an unspecified label is encountered (default is
                        to ignore) (default: False)
  --labels LABEL [LABEL ...]
                        specifies the labels for each index (default: None)
```

### PASSTHROUGH
Dummy ISP which has no effect on the conversion stream

#### Domain(s):
- **Image Segmentation Domain**
- **Image Object-Detection Domain**
- **Speech Domain**
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
                        the maximum number of points in the polygon (default: None)
  --min-points MIN_POINTS
                        the minimum number of points in the polygon (default: None)
  --verbose             outputs information when discarding annotations (default: False)
```

### REDIS-PREDICT-IC
Makes image classification predictions via Redis backend, passing in an image and receiving JSON predictions back (at least one of 'label: probability').
Predictions example:
{"dog": 0.9, "cat": 0.1}

#### Domain(s):
- **Image Classification Domain**

#### Options:
```
usage: redis-predict-ic [--channel-in CHANNEL_IN] [--channel-out CHANNEL_OUT] [-d REDIS_DB]
                        [-h REDIS_HOST] [-p REDIS_PORT] [-t TIMEOUT] [-v]

optional arguments:
  --channel-in CHANNEL_IN
                        the Redis channel on which to receive predictions. (default: predictions)
  --channel-out CHANNEL_OUT
                        the Redis channel to send the images out (default: images)
  -d REDIS_DB, --redis-db REDIS_DB
                        the database to use (default: 0)
  -h REDIS_HOST, --redis-host REDIS_HOST
                        the Redis server to connect to (default: localhost)
  -p REDIS_PORT, --redis-port REDIS_PORT
                        the port the Redis server is running on (default: 6379)
  -t TIMEOUT, --timeout TIMEOUT
                        the timeout in seconds to wait for a prediction to arrive (default: 5.0)
  -v, --verbose         whether to output debugging information. (default: False)
```

### REDIS-PREDICT-IS
Makes image segmentation predictions via Redis backend, passing in an image and receiving an image with predicted segmentations.

#### Domain(s):
- **Image Segmentation Domain**

#### Options:
```
usage: redis-predict-is [--channel-in CHANNEL_IN] [--channel-out CHANNEL_OUT]
                        [--image-format IMAGE_FORMAT] --labels LABEL [LABEL ...] [-d REDIS_DB]
                        [-h REDIS_HOST] [-p REDIS_PORT] [-t TIMEOUT] [-v]

optional arguments:
  --channel-in CHANNEL_IN
                        the Redis channel on which to receive predictions. (default: predictions)
  --channel-out CHANNEL_OUT
                        the Redis channel to send the images out (default: images)
  --image-format IMAGE_FORMAT
                        the format of the image that comes back as prediction:
                        indexedpng,bluechannel,grayscale (default: indexedpng)
  --labels LABEL [LABEL ...]
                        specifies the labels for each index (default: None)
  -d REDIS_DB, --redis-db REDIS_DB
                        the database to use (default: 0)
  -h REDIS_HOST, --redis-host REDIS_HOST
                        the Redis server to connect to (default: localhost)
  -p REDIS_PORT, --redis-port REDIS_PORT
                        the port the Redis server is running on (default: 6379)
  -t TIMEOUT, --timeout TIMEOUT
                        the timeout in seconds to wait for a prediction to arrive (default: 5.0)
  -v, --verbose         whether to output debugging information. (default: False)
```

### REDIS-PREDICT-OD
Makes object detection predictions via Redis backend, passing in an image and receiving OPEX predictions back:
https://github.com/WaikatoLink2020/objdet-predictions-exchange-format

#### Domain(s):
- **Image Object-Detection Domain**

#### Options:
```
usage: redis-predict-od [--channel-in CHANNEL_IN] [--channel-out CHANNEL_OUT]
                        [--key-label KEY_LABEL] [--key-score KEY_SCORE] [-d REDIS_DB]
                        [-h REDIS_HOST] [-p REDIS_PORT] [-t TIMEOUT] [-v]

optional arguments:
  --channel-in CHANNEL_IN
                        the Redis channel on which to receive predictions. (default: predictions)
  --channel-out CHANNEL_OUT
                        the Redis channel to send the images out (default: images)
  --key-label KEY_LABEL
                        the meta-data key in the annotations to use for storing the label. (default:
                        type)
  --key-score KEY_SCORE
                        the meta-data key in the annotations to use for storing the prediction
                        score. (default: score)
  -d REDIS_DB, --redis-db REDIS_DB
                        the database to use (default: 0)
  -h REDIS_HOST, --redis-host REDIS_HOST
                        the Redis server to connect to (default: localhost)
  -p REDIS_PORT, --redis-port REDIS_PORT
                        the port the Redis server is running on (default: 6379)
  -t TIMEOUT, --timeout TIMEOUT
                        the timeout in seconds to wait for a prediction to arrive (default: 5.0)
  -v, --verbose         whether to output debugging information. (default: False)
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
                        the classes to remove (default: None)
```

### ROTATE
Rotates images randomly within a range of degrees or by a specified degree. Specify seed value and force augmentation to be seeded to generate repeatable augmentations.

#### Domain(s):
- **Image Object-Detection Domain**
- **Image Classification Domain**

#### Options:
```
usage: rotate [-f DEGREE_FROM] [-t DEGREE_TO] [-m IMGAUG_MODE] [--suffix IMGAUG_SUFFIX] [-s SEED]
              [-a] [-T THRESHOLD]

optional arguments:
  -f DEGREE_FROM, --from-degree DEGREE_FROM
                        the start of the degree range to use for rotating the images (default: None)
  -t DEGREE_TO, --to-degree DEGREE_TO
                        the end of the degree range to use for rotating the images (default: None)
  -m IMGAUG_MODE, --mode IMGAUG_MODE
                        the image augmentation mode to use, available modes: replace, add (default:
                        replace)
  --suffix IMGAUG_SUFFIX
                        the suffix to use for the file names in case of augmentation mode add
                        (default: None)
  -s SEED, --seed SEED  the seed value to use for the random number generator; randomly seeded if
                        not provided (default: None)
  -a, --seed-augmentation
                        whether to seed the augmentation; if specified, uses the seeded random
                        generator to produce a seed value from 0 to 1000 for the augmentation.
                        (default: False)
  -T THRESHOLD, --threshold THRESHOLD
                        the threshold to use for Random.rand(): if equal or above, augmentation gets
                        applied; range: 0-1; default: 0 (= always) (default: None)
```

### SCALE
Scales images randomly within a range of percentages or by a specified percentage. Specify seed value and force augmentation to be seeded to generate repeatable augmentations.

#### Domain(s):
- **Image Object-Detection Domain**
- **Image Classification Domain**

#### Options:
```
usage: scale [-m IMGAUG_MODE] [--suffix IMGAUG_SUFFIX] [-k] [-f PERCENTAGE_FROM] [-t PERCENTAGE_TO]
             [-s SEED] [-a] [-T THRESHOLD] [-u]

optional arguments:
  -m IMGAUG_MODE, --mode IMGAUG_MODE
                        the image augmentation mode to use, available modes: replace, add (default:
                        replace)
  --suffix IMGAUG_SUFFIX
                        the suffix to use for the file names in case of augmentation mode add
                        (default: None)
  -k, --keep-aspect     whether to keep the aspect ratio (default: False)
  -f PERCENTAGE_FROM, --from-percentage PERCENTAGE_FROM
                        the start of the percentage range to use for scaling the images (default:
                        None)
  -t PERCENTAGE_TO, --to-percentage PERCENTAGE_TO
                        the end of the percentage range to use for scaling the images (default:
                        None)
  -s SEED, --seed SEED  the seed value to use for the random number generator; randomly seeded if
                        not provided (default: None)
  -a, --seed-augmentation
                        whether to seed the augmentation; if specified, uses the seeded random
                        generator to produce a seed value from 0 to 1000 for the augmentation.
                        (default: False)
  -T THRESHOLD, --threshold THRESHOLD
                        the threshold to use for Random.rand(): if equal or above, augmentation gets
                        applied; range: 0-1; default: 0 (= always) (default: None)
  -u, --update-size     whether to update the image size after the scaling operation or use original
                        size (default: False)
```

### SKIP-SIMILAR-FRAMES
Skips frames in the stream that are deemed too similar.

#### Domain(s):
- **Image Segmentation Domain**
- **Image Object-Detection Domain**
- **Image Classification Domain**

#### Options:
```
usage: skip-similar-frames [-b BW_THRESHOLD] [-t CHANGE_THRESHOLD] [-c CONVERSION] [-v]

optional arguments:
  -b BW_THRESHOLD, --bw-threshold BW_THRESHOLD
                        the threshold to use for converting a gray-scale like image to black and
                        white (0-255) (default: 128)
  -t CHANGE_THRESHOLD, --change-threshold CHANGE_THRESHOLD
                        the percentage of pixels that changed relative to size of image (0-1)
                        (default: 0.01)
  -c CONVERSION, --conversion CONVERSION
                        how to convert the BGR image to a single channel image (gray/r/g/b)
                        (default: gray)
  -v, --verbose         whether to output some debugging output. (default: False)
```

### STRIP-ANNOTATIONS
ISP which removes annotations from instances

#### Domain(s):
- **Image Segmentation Domain**
- **Image Object-Detection Domain**
- **Speech Domain**
- **Image Classification Domain**

#### Options:
```
usage: strip-annotations
```

### SUB-IMAGES
Extracts sub-images (incl their annotations) from the images coming through, using the defined regions.

#### Domain(s):
- **Image Object-Detection Domain**
- **Image Classification Domain**

#### Options:
```
usage: sub-images [-p] [-s REGION_SORTING] [-r REGIONS [REGIONS ...]] [-e]

optional arguments:
  -p, --include-partial
                        whether to include only annotations that fit fully into a region or also
                        partial ones (default: False)
  -s REGION_SORTING, --region-sorting REGION_SORTING
                        how to sort the supplied region definitions: none|x-then-y|y-then-x
                        (default: none)
  -r REGIONS [REGIONS ...], --regions REGIONS [REGIONS ...]
                        the regions (X,Y,WIDTH,HEIGHT) to crop and forward with their annotations
                        (default: [])
  -e, --suppress-empty  suppresses sub-images that have no annotations (object detection) (default:
                        False)
```


## Sink stage
### AREA-HISTOGRAM-IS
Generates histograms of the area (normalized or absolute) occupied by the annotations.

#### Domain(s):
- **Image Segmentation Domain**

#### Options:
```
usage: area-histogram-is [-a ALL_LABEL] [-b] [--label-key LABEL_KEY] [-n] [--num-bins NUM_BINS]
                         [-o OUTPUT_FILE] [-f OUTPUT_FORMAT]

optional arguments:
  -a ALL_LABEL, --all-label ALL_LABEL
                        the label to use for all the labels combined (default: ALL)
  -b, --force-bbox      whether to use the bounding box even if a polygon is present (object
                        detection domain only) (default: False)
  --label-key LABEL_KEY
                        the key in the meta-data that contains the label. (default: type)
  -n, --normalized      whether to use normalized areas (using the image size as base). (default:
                        False)
  --num-bins NUM_BINS   the number of bins to use for the histogram. (default: 20)
  -o OUTPUT_FILE, --output OUTPUT_FILE
                        the file to write the histogram to; uses stdout if omitted (default: )
  -f OUTPUT_FORMAT, --format OUTPUT_FORMAT
                        the format to use for the output, available modes: csv, json (default: text)
```

### AREA-HISTOGRAM-OD
Generates histograms of the area (normalized or absolute) occupied by the annotations.

#### Domain(s):
- **Image Object-Detection Domain**

#### Options:
```
usage: area-histogram-od [-a ALL_LABEL] [-b] [--label-key LABEL_KEY] [-n] [--num-bins NUM_BINS]
                         [-o OUTPUT_FILE] [-f OUTPUT_FORMAT]

optional arguments:
  -a ALL_LABEL, --all-label ALL_LABEL
                        the label to use for all the labels combined (default: ALL)
  -b, --force-bbox      whether to use the bounding box even if a polygon is present (object
                        detection domain only) (default: False)
  --label-key LABEL_KEY
                        the key in the meta-data that contains the label. (default: type)
  -n, --normalized      whether to use normalized areas (using the image size as base). (default:
                        False)
  --num-bins NUM_BINS   the number of bins to use for the histogram. (default: 20)
  -o OUTPUT_FILE, --output OUTPUT_FILE
                        the file to write the histogram to; uses stdout if omitted (default: )
  -f OUTPUT_FORMAT, --format OUTPUT_FORMAT
                        the format to use for the output, available modes: csv, json (default: text)
```

### CALC-FRAME-CHANGES
Calculates the changes between frames, which can be used with the skip-similar-frames ISP.

#### Domain(s):
- **Image Object-Detection Domain**

#### Options:
```
usage: calc-frame-changes [-b BW_THRESHOLD] [-t CHANGE_THRESHOLD] [-c CONVERSION] [-B NUM_BINS]
                          [-o OUTPUT_FILE] [-f OUTPUT_FORMAT] [-v]

optional arguments:
  -b BW_THRESHOLD, --bw-threshold BW_THRESHOLD
                        the threshold to use for converting a gray-scale like image to black and
                        white (0-255) (default: 128)
  -t CHANGE_THRESHOLD, --change-threshold CHANGE_THRESHOLD
                        the percentage of pixels that changed relative to size of image (0-1)
                        (default: 0.01)
  -c CONVERSION, --conversion CONVERSION
                        how to convert the BGR image to a single channel image (gray/r/g/b)
                        (default: gray)
  -B NUM_BINS, --num-bins NUM_BINS
                        the number of bins to use for the histogram (default: 20)
  -o OUTPUT_FILE, --output OUTPUT_FILE
                        the file to write to statistics to, stdout if not provided (default: )
  -f OUTPUT_FORMAT, --output-format OUTPUT_FORMAT
                        how to output the statistics (text/csv/json) (default: text)
  -v, --verbose         whether to output some debugging output. (default: False)
```

### IMAGE-VIEWER-IC
Displays image classification images.

#### Domain(s):
- **Image Classification Domain**

#### Options:
```
usage: image-viewer-ic [--delay DELAY] [--position POSITION] [--size SIZE] [--title TITLE]

optional arguments:
  --delay DELAY        the delay in milli-seconds between images, use 0 to wait for keypress,
                       ignored if <0 (default: 500)
  --position POSITION  the position of the window on screen (X,Y) (default: 0,0)
  --size SIZE          the maximum size for the image: WIDTH,HEIGHT (default: 640,480)
  --title TITLE        the title for the window (default: wai.annotations)
```

### IMAGE-VIEWER-IS
Displays image segmentation images.

#### Domain(s):
- **Image Segmentation Domain**

#### Options:
```
usage: image-viewer-is [--delay DELAY] [--position POSITION] [--size SIZE] [--title TITLE]

optional arguments:
  --delay DELAY        the delay in milli-seconds between images, use 0 to wait for keypress,
                       ignored if <0 (default: 500)
  --position POSITION  the position of the window on screen (X,Y) (default: 0,0)
  --size SIZE          the maximum size for the image: WIDTH,HEIGHT (default: 640,480)
  --title TITLE        the title for the window (default: wai.annotations)
```

### IMAGE-VIEWER-OD
Displays object detection images.

#### Domain(s):
- **Image Object-Detection Domain**

#### Options:
```
usage: image-viewer-od [--delay DELAY] [--position POSITION] [--size SIZE] [--title TITLE]

optional arguments:
  --delay DELAY        the delay in milli-seconds between images, use 0 to wait for keypress,
                       ignored if <0 (default: 500)
  --position POSITION  the position of the window on screen (X,Y) (default: 0,0)
  --size SIZE          the maximum size for the image: WIDTH,HEIGHT (default: 640,480)
  --title TITLE        the title for the window (default: wai.annotations)
```

### LABEL-DIST-IC
Generates a label distribution.

#### Domain(s):
- **Image Classification Domain**

#### Options:
```
usage: label-dist-ic [--label-key LABEL_KEY] [-o OUTPUT_FILE] [-f OUTPUT_FORMAT] [-p]

optional arguments:
  --label-key LABEL_KEY
                        the key in the meta-data that contains the label. (default: type)
  -o OUTPUT_FILE, --output OUTPUT_FILE
                        the file to write the statistics to; uses stdout if omitted (default: )
  -f OUTPUT_FORMAT, --format OUTPUT_FORMAT
                        the format to use for the output, available modes: csv, json (default: text)
  -p, --percentages     whether to output percentages instead of counts. (default: False)
```

### LABEL-DIST-IS
Generates a label distribution.

#### Domain(s):
- **Image Segmentation Domain**

#### Options:
```
usage: label-dist-is [--label-key LABEL_KEY] [-o OUTPUT_FILE] [-f OUTPUT_FORMAT] [-p]

optional arguments:
  --label-key LABEL_KEY
                        the key in the meta-data that contains the label. (default: type)
  -o OUTPUT_FILE, --output OUTPUT_FILE
                        the file to write the statistics to; uses stdout if omitted (default: )
  -f OUTPUT_FORMAT, --format OUTPUT_FORMAT
                        the format to use for the output, available modes: csv, json (default: text)
  -p, --percentages     whether to output percentages instead of counts. (default: False)
```

### LABEL-DIST-OD
Generates a label distribution.

#### Domain(s):
- **Image Object-Detection Domain**

#### Options:
```
usage: label-dist-od [--label-key LABEL_KEY] [-o OUTPUT_FILE] [-f OUTPUT_FORMAT] [-p]

optional arguments:
  --label-key LABEL_KEY
                        the key in the meta-data that contains the label. (default: type)
  -o OUTPUT_FILE, --output OUTPUT_FILE
                        the file to write the statistics to; uses stdout if omitted (default: )
  -f OUTPUT_FORMAT, --format OUTPUT_FORMAT
                        the format to use for the output, available modes: csv, json (default: text)
  -p, --percentages     whether to output percentages instead of counts. (default: False)
```

### TO-ADAMS-IC
Writes image classification annotations in the ADAMS report-format

#### Domain(s):
- **Image Classification Domain**

#### Options:
```
usage: to-adams-ic -c FIELD [--annotations-only] -o PATH [--split-names SPLIT NAME [SPLIT NAME ...]]
                   [--split-ratios RATIO [RATIO ...]]

optional arguments:
  -c FIELD, --class-field FIELD
                        the report field containing the image class (default: None)
  --annotations-only    skip the writing of data files, outputting only the annotation files
                        (default: False)
  -o PATH, --output PATH
                        output directory to write files to (default: None)
  --split-names SPLIT NAME [SPLIT NAME ...]
                        the names to use for the splits (default: [])
  --split-ratios RATIO [RATIO ...]
                        the ratios to use for the splits (default: [])
```

### TO-ADAMS-OD
Writes image object-detection annotations in the ADAMS report-format

#### Domain(s):
- **Image Object-Detection Domain**

#### Options:
```
usage: to-adams-od [--annotations-only] -o PATH [--split-names SPLIT NAME [SPLIT NAME ...]]
                   [--split-ratios RATIO [RATIO ...]]

optional arguments:
  --annotations-only    skip the writing of data files, outputting only the annotation files
                        (default: False)
  -o PATH, --output PATH
                        output directory to write files to (default: None)
  --split-names SPLIT NAME [SPLIT NAME ...]
                        the names to use for the splits (default: [])
  --split-ratios RATIO [RATIO ...]
                        the ratios to use for the splits (default: [])
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
                        the color to use for the background as RGBA byte-quadruplet, e.g.:
                        255,255,255,255 (default: 255,255,255,255)
  -c COLOR, --color COLOR
                        the color to use for drawing the shapes as RGBA byte-quadruplet, e.g.:
                        255,0,0,64 (default: 255,0,0,64)
  -o OUTPUT_FILE, --output OUTPUT_FILE
                        the PNG image to write the generated overlay to (default: ./overlay.png)
  -s SCALE_TO, --scale-to SCALE_TO
                        the dimensions to scale all images to before overlaying them (format:
                        width,height) (default: )
```

### TO-BLUE-CHANNEL-IS
Writes image segmentation files in the blue-channel format

#### Domain(s):
- **Image Segmentation Domain**

#### Options:
```
usage: to-blue-channel-is [--annotations-only] -o PATH [--split-names SPLIT NAME [SPLIT NAME ...]]
                          [--split-ratios RATIO [RATIO ...]]

optional arguments:
  --annotations-only    skip the writing of data files, outputting only the annotation files
                        (default: False)
  -o PATH, --output PATH
                        the directory to write the annotation images to (default: None)
  --split-names SPLIT NAME [SPLIT NAME ...]
                        the names to use for the splits (default: [])
  --split-ratios RATIO [RATIO ...]
                        the ratios to use for the splits (default: [])
```

### TO-COCO-OD
Writes image object-detection annotations in the MS-COCO JSON-format

#### Domain(s):
- **Image Object-Detection Domain**

#### Options:
```
usage: to-coco-od [--annotations-only] [--categories CATEGORY [CATEGORY ...]]
                  [--category-output-file FILENAME] [--default-supercategory SUPERCATEGORY]
                  [--error-on-new-category] [--license-name LICENSE_NAME]
                  [--license-url LICENSE_URL] -o PATH [--pretty] [--sort-categories]
                  [--split-names SPLIT NAME [SPLIT NAME ...]] [--split-ratios RATIO [RATIO ...]]

optional arguments:
  --annotations-only    skip the writing of data files, outputting only the annotation files
                        (default: False)
  --categories CATEGORY [CATEGORY ...]
                        defines the order of the categories (default: [])
  --category-output-file FILENAME
                        file to write the categories into, as a simple comma-separated list
                        (default: None)
  --default-supercategory SUPERCATEGORY
                        the supercategory to use for pre-defined categories (default: Object)
  --error-on-new-category
                        whether unspecified categories should raise an error (default: False)
  --license-name LICENSE_NAME
                        the license of the images (default: default)
  --license-url LICENSE_URL
                        the license of the images (default: )
  -o PATH, --output PATH
                        output file to write annotations to (images are placed in same directory)
                        (default: None)
  --pretty              whether to format the JSON annotations file with indentation (default:
                        False)
  --sort-categories     whether to put the categories in alphabetical order (default: False)
  --split-names SPLIT NAME [SPLIT NAME ...]
                        the names to use for the splits (default: [])
  --split-ratios RATIO [RATIO ...]
                        the ratios to use for the splits (default: [])
```

### TO-COMMON-VOICE-SP
Writes speech transcriptions in the Mozilla Common-Voice TSV-format

#### Domain(s):
- **Speech Domain**

#### Options:
```
usage: to-common-voice-sp [--annotations-only] -o PATH [--split-names SPLIT NAME [SPLIT NAME ...]]
                          [--split-ratios RATIO [RATIO ...]]

optional arguments:
  --annotations-only    skip the writing of data files, outputting only the annotation files
                        (default: False)
  -o PATH, --output PATH
                        the filename of the TSV file to write the annotations into (default: None)
  --split-names SPLIT NAME [SPLIT NAME ...]
                        the names to use for the splits (default: [])
  --split-ratios RATIO [RATIO ...]
                        the ratios to use for the splits (default: [])
```

### TO-FESTVOX-SP
Writes speech transcriptions in the Festival FestVox format

#### Domain(s):
- **Speech Domain**

#### Options:
```
usage: to-festvox-sp [--annotations-only] -o PATH [--split-names SPLIT NAME [SPLIT NAME ...]]
                     [--split-ratios RATIO [RATIO ...]]

optional arguments:
  --annotations-only    skip the writing of data files, outputting only the annotation files
                        (default: False)
  -o PATH, --output PATH
                        the filename of the FestVox file to write the annotations into (default:
                        None)
  --split-names SPLIT NAME [SPLIT NAME ...]
                        the names to use for the splits (default: [])
  --split-ratios RATIO [RATIO ...]
                        the ratios to use for the splits (default: [])
```

### TO-GRAYSCALE-IS
Writes image segmentation files in the grayscale format

#### Domain(s):
- **Image Segmentation Domain**

#### Options:
```
usage: to-grayscale-is [--annotations-only] -o PATH [--split-names SPLIT NAME [SPLIT NAME ...]]
                       [--split-ratios RATIO [RATIO ...]]

optional arguments:
  --annotations-only    skip the writing of data files, outputting only the annotation files
                        (default: False)
  -o PATH, --output PATH
                        the directory to write the annotation images to (default: None)
  --split-names SPLIT NAME [SPLIT NAME ...]
                        the names to use for the splits (default: [])
  --split-ratios RATIO [RATIO ...]
                        the ratios to use for the splits (default: [])
```

### TO-IMAGES-IC
Dummy writer that just outputs images from image classification datasets.

#### Domain(s):
- **Image Classification Domain**

#### Options:
```
usage: to-images-ic [-o OUTPUT_DIR]

optional arguments:
  -o OUTPUT_DIR, --output-dir OUTPUT_DIR
                        the directory to write the images to (default: .)
```

### TO-IMAGES-IS
Dummy writer that just outputs images from image segmentation datasets.

#### Domain(s):
- **Image Segmentation Domain**

#### Options:
```
usage: to-images-is [-o OUTPUT_DIR]

optional arguments:
  -o OUTPUT_DIR, --output-dir OUTPUT_DIR
                        the directory to write the images to (default: .)
```

### TO-IMAGES-OD
Dummy writer that just outputs images from object detection datasets.

#### Domain(s):
- **Image Object-Detection Domain**

#### Options:
```
usage: to-images-od [-o OUTPUT_DIR]

optional arguments:
  -o OUTPUT_DIR, --output-dir OUTPUT_DIR
                        the directory to write the images to (default: .)
```

### TO-INDEXED-PNG-IS
Writes image segmentation files in the indexed-PNG format

#### Domain(s):
- **Image Segmentation Domain**

#### Options:
```
usage: to-indexed-png-is [--annotations-only] -o PATH [--split-names SPLIT NAME [SPLIT NAME ...]]
                         [--split-ratios RATIO [RATIO ...]]

optional arguments:
  --annotations-only    skip the writing of data files, outputting only the annotation files
                        (default: False)
  -o PATH, --output PATH
                        the directory to write the annotation images to (default: None)
  --split-names SPLIT NAME [SPLIT NAME ...]
                        the names to use for the splits (default: [])
  --split-ratios RATIO [RATIO ...]
                        the ratios to use for the splits (default: [])
```

### TO-LAYER-SEGMENTS-IS
Writes the layer-segments image-segmentation format to disk

#### Domain(s):
- **Image Segmentation Domain**

#### Options:
```
usage: to-layer-segments-is [--annotations-only] [--label-separator SEPARATOR] -o PATH
                            [--split-names SPLIT NAME [SPLIT NAME ...]]
                            [--split-ratios RATIO [RATIO ...]]

optional arguments:
  --annotations-only    skip the writing of data files, outputting only the annotation files
                        (default: False)
  --label-separator SEPARATOR
                        the separator between the base filename and the label (default: -)
  -o PATH, --output PATH
                        the directory to write the annotation images to (default: None)
  --split-names SPLIT NAME [SPLIT NAME ...]
                        the names to use for the splits (default: [])
  --split-ratios RATIO [RATIO ...]
                        the ratios to use for the splits (default: [])
```

### TO-OPEX-OD
Writes image object-detection annotations in the OPEX format

#### Domain(s):
- **Image Object-Detection Domain**

#### Options:
```
usage: to-opex-od [-c PATH] [-l PATH] [--annotations-only] -o PATH
                  [--split-names SPLIT NAME [SPLIT NAME ...]] [--split-ratios RATIO [RATIO ...]]

optional arguments:
  -c PATH, --labels-csv PATH
                        Path to the labels CSV file to write (default: None)
  -l PATH, --labels PATH
                        Path to the labels file to write (default: None)
  --annotations-only    skip the writing of data files, outputting only the annotation files
                        (default: False)
  -o PATH, --output PATH
                        output directory to write images and annotations to (default: None)
  --split-names SPLIT NAME [SPLIT NAME ...]
                        the names to use for the splits (default: [])
  --split-ratios RATIO [RATIO ...]
                        the ratios to use for the splits (default: [])
```

### TO-ROI-OD
Writes image object-detection annotations in the ROI CSV-format

#### Domain(s):
- **Image Object-Detection Domain**

#### Options:
```
usage: to-roi-od [-d WIDTH HEIGHT] [--annotations-only] [--comments COMMENTS [COMMENTS ...]] -o PATH
                 [--size-mode] [--split-names SPLIT NAME [SPLIT NAME ...]]
                 [--split-ratios RATIO [RATIO ...]] [--prefix WRITER_PREFIX]
                 [--suffix WRITER_SUFFIX]

optional arguments:
  -d WIDTH HEIGHT, --image-dimensions WIDTH HEIGHT
                        image dimensions to use if none can be inferred (default: [])
  --annotations-only    skip the writing of data files, outputting only the annotation files
                        (default: False)
  --comments COMMENTS [COMMENTS ...]
                        comments to write to the beginning of the ROI file (default: [])
  -o PATH, --output PATH
                        output directory to write files to (default: None)
  --size-mode           writes the ROI files with x,y,w,h headers instead of x0,y0,x1,y1 (default:
                        False)
  --split-names SPLIT NAME [SPLIT NAME ...]
                        the names to use for the splits (default: [])
  --split-ratios RATIO [RATIO ...]
                        the ratios to use for the splits (default: [])
  --prefix WRITER_PREFIX
                        the prefix for output filenames (default = '') (default: None)
  --suffix WRITER_SUFFIX
                        the suffix for output filenames (default = '-rois.csv') (default: None)
```

### TO-SUBDIR-IC
Writes images to sub-directories named after their class labels.

#### Domain(s):
- **Image Classification Domain**

#### Options:
```
usage: to-subdir-ic -o PATH [--split-names SPLIT NAME [SPLIT NAME ...]]
                    [--split-ratios RATIO [RATIO ...]]

optional arguments:
  -o PATH, --output PATH
                        the directory to store the class directories in (default: None)
  --split-names SPLIT NAME [SPLIT NAME ...]
                        the names to use for the splits (default: [])
  --split-ratios RATIO [RATIO ...]
                        the ratios to use for the splits (default: [])
```

### TO-TF-OD
Writes image object-detection annotations in the TFRecords binary format

#### Domain(s):
- **Image Object-Detection Domain**

#### Options:
```
usage: to-tf-od [--dense] [--source-id-type {filename,numeric-dummy}] -o PATH [-p FILENAME]
                [-s FILENAME [FILENAME ...]] [--split-names SPLIT NAME [SPLIT NAME ...]]
                [--split-ratios RATIO [RATIO ...]]

optional arguments:
  --dense               outputs masks in the dense numerical format instead of PNG-encoded (default:
                        False)
  --source-id-type {filename,numeric-dummy}
                        by default, the filename gets stored in the 'source_id' field, but some
                        algorithms try to convert it into a number and fail with 'StringToNumberOp
                        could not correctly convert string'; in which case you can use 'numeric-
                        dummy' (see https://github.com/google/automl/issues/307) (default: filename)
  -o PATH, --output PATH
                        name of output file for TFRecords (default: None)
  -p FILENAME, --protobuf FILENAME
                        for storing the label strings and IDs (default: None)
  -s FILENAME [FILENAME ...], --shards FILENAME [FILENAME ...]
                        additional shards to write to (default: [])
  --split-names SPLIT NAME [SPLIT NAME ...]
                        the names to use for the splits (default: [])
  --split-ratios RATIO [RATIO ...]
                        the ratios to use for the splits (default: [])
```

### TO-VGG-OD
Writes image object-detection annotations in the VGG JSON-format

#### Domain(s):
- **Image Object-Detection Domain**

#### Options:
```
usage: to-vgg-od [--annotations-only] -o PATH [--pretty] [--split-names SPLIT NAME [SPLIT NAME ...]]
                 [--split-ratios RATIO [RATIO ...]]

optional arguments:
  --annotations-only    skip the writing of data files, outputting only the annotation files
                        (default: False)
  -o PATH, --output PATH
                        output file to write annotations to (images are placed in same directory)
                        (default: None)
  --pretty              whether to format the JSON annotations file with indentation (default:
                        False)
  --split-names SPLIT NAME [SPLIT NAME ...]
                        the names to use for the splits (default: [])
  --split-ratios RATIO [RATIO ...]
                        the ratios to use for the splits (default: [])
```

### TO-VIDEO-FILE-OD
Writes frames to a MJPG video file.

#### Domain(s):
- **Image Object-Detection Domain**

#### Options:
```
usage: to-video-file-od [-f FPS] [-o OUTPUT_FILE]

optional arguments:
  -f FPS, --fps FPS     the frames per second to use (default: 25)
  -o OUTPUT_FILE, --output OUTPUT_FILE
                        the MJPG video file to write to (default: )
```

### TO-VOC-OD
Writes image object-detection annotations in the Pascal VOC XML-format

#### Domain(s):
- **Image Object-Detection Domain**

#### Options:
```
usage: to-voc-od [--annotations-only] -o PATH [--split-names SPLIT NAME [SPLIT NAME ...]]
                 [--split-ratios RATIO [RATIO ...]]

optional arguments:
  --annotations-only    skip the writing of data files, outputting only the annotation files
                        (default: False)
  -o PATH, --output PATH
                        output directory to write annotations to (images are placed in same
                        directory) (default: None)
  --split-names SPLIT NAME [SPLIT NAME ...]
                        the names to use for the splits (default: [])
  --split-ratios RATIO [RATIO ...]
                        the ratios to use for the splits (default: [])
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
usage: to-yolo-od [-c PATH] [-l PATH] [--annotations-only] -o PATH
                  [--split-names SPLIT NAME [SPLIT NAME ...]] [--split-ratios RATIO [RATIO ...]]

optional arguments:
  -c PATH, --labels-csv PATH
                        Path to the labels CSV file to write (default: None)
  -l PATH, --labels PATH
                        Path to the labels file to write (default: None)
  --annotations-only    skip the writing of data files, outputting only the annotation files
                        (default: False)
  -o PATH, --output PATH
                        output directory to write images and annotations to (default: None)
  --split-names SPLIT NAME [SPLIT NAME ...]
                        the names to use for the splits (default: [])
  --split-ratios RATIO [RATIO ...]
                        the ratios to use for the splits (default: [])
```
