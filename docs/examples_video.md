# Read frames from a video file

The following command retrieves every 10th frame (`-n`) from the input video, 
will process a maximum of 100 frames (`-m`) and will process frames 
starting from 1000 (`-f`) and display the frames ([example video](https://github.com/lessthanoptimal/BoofCV-Data/blob/15c79700a26646ed33806fe9e834e0224acb75c8/example/tracking/dashcam01.mp4)):

```bash
wai-annotations convert \
  from-video-file-od \
    -i "./video/dashcam01.mp4" \
    -n 10 \
    -m 100 \
    -f 1000 \
  image-viewer-od
```

# Read frames from a webcam

A webcam can also be used for obtaining frames, as the following example demonstrates 
(uses webcam with ID `0`): 

```bash
wai-annotations convert \
  from-webcam-od \
    -i 0 \
    -n 10 \
    -m 100 \
    -f 100 
  image-viewer-od
```

# Generate a MJPEG video file of dissimilar frames

Videos contain a lot of frames and outputting or processing all of them is not
a viable option in most cases. For that purpose, the `skip-similar-frames` plugin
can be used for dropping frames that are too similar. The `-t/--change-threshold`
parameter determines how sensitive to change the plugin is (ratio of pixels that 
are different between images). The subset of frames is written to a MJPEG video
file with 1 frame/sec:

```bash
wai-annotations convert \
  from-video-file-od \
    -i "./video/some_video.mp4" \
  skip-similar-frames \
    --change-threshold 0.03 \ 
    --verbose \
  to-video-file-od \
    -f 1 \
    -o ./out.mjpeg
```
