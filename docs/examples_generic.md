The purpose of [wai.annotations.generic](https://github.com/waikato-ufdl/wai-annotations-generic)
module is to make it easier to integrate custom operators quickly into wai.annotations. 

By providing generic wrappers for sources, ISPs and sinks, you only need to implement a class that
is derived from the correct wai.annotations superclass(es), add it to the `PYTHONPATH` and supplying
class name and options to the appropriate generic wrapper plugin.

The following example wraps a [test source class](https://github.com/waikato-ufdl/wai-annotations-generic/blob/main/src/wai/annotations/generic/source/image_classification/test/_TestIC.py)
and a [test ISP class](https://github.com/waikato-ufdl/wai-annotations-generic/blob/main/src/wai/annotations/generic/isp/image_classification/test/_TestIC.py)
and makes them available from the command-line as follows:

```bash
wai-annotations convert \
  generic-source-ic \
    -c wai.annotations.generic.source.image_classification.test.TestIC \
    -o "--dir /some/where/" \  # dir with .jpg files
  generic-sink-ic \
    -c wai.annotations.generic.sink.image_classification.test.TestIC \
    -o "--output label"
```
