The following example converts a single MP3 file to WAV (`convert-to-wav`), ensures that it is
monophonic (`convert-to-mono`) and resamples it to 11khz (`resample-audio`) before saving it.

```bash
wai-annotations convert \
  from-audio-files-ac \
    -i "/some/where/an.mp3" \
  convert-to-wav \
  convert-to-mono \
  resample-audio \
    --sample-rate 11000 \
  to-audio-files-ac \
    -o /some/where/else/
```

When splitting up samples into sub-samples (automatically or by a human), it can
happen quite often that there is silence at the start and/or at the end of the clip.
The `trim-audio` plugin can be used to remove these (the minimum decibel level can 
be supplied as parameter):

```bash
wai-annotations convert \
  from-audio-files-ac \
    -i "/some/where/an.mp3" \
  convert-to-wav \
  convert-to-mono \
  resample-audio \
    --sample-rate 11000 \
  to-audio-files-ac \
    -o /some/where/else/
```

Audio augmentation is possible as well. The `pitch-shift` plugin changes the pitch of
the sample and `time-stretch` can slow down or speed up the sample (using `-T 0` for 
the threshold means it gets always applied):

```bash
wai-annotations convert \
  from-audio-files-ac \
    -i "/some/where/a.wav" \
  pitch-shift \
    -m add \
    -f 4 \
    -t 4 \
    -T 0 \
  time-stretch\
    -m add \
    -f 0.5 \
    -t 2.0 \
    -T 0 \
  to-audio-files-ac \
    -o /some/where/else/
```

Spectrograms from the audio samples can be generated using the `stft-spectrogram`
and `mel-spectrogram` plugins:

```bash
wai-annotations convert \
  from-audio-files-ac \
    -i "/some/where/a.wav" \
  stft-spectrogram \
  to-images-ic \
    -o /some/where/else/
```

If the [wai.annotations.generic](https://github.com/waikato-ufdl/wai-annotations-generic) module
is installed, then it is possible to take advantage of the `wai.annotations.audio.source.urban8k.Urban8k`
example class for loading the [Urban8k](https://urbansounddataset.weebly.com/urbansound8k.html).
Using the [wai.annotations.subdir](https://github.com/waikato-ufdl/wai-annotations-subdir) module,
the .wav files can be stored in sub-directories according to their class labels:

```bash
wai-annotations convert \
  generic-source-ac \
    -c "wai.annotations.audio.source.urban8k.Urban8k" \
    -o "--metadata-csv /some/where/UrbanSound8K/metadata/UrbanSound8K.csv --fold-dir /some/where/UrbanSound8K/audio/" \
  to-subdir-ac \
    -o /some/where/else/urban8k
```
