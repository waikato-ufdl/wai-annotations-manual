# Installation of wai-annotations

To install wai-annotations issue the following commands using pip:

```commandline
pip install wai.annotations.core
```

`wai.annotations.core` does not come with any input/output formats installed. You will need to install a plugin for each
format that you want to convert between. For a description of the plugin system, see the [plugin guide](plugin.md).

For installing all available plugins, use this command:

```commandline
pip install wai.annotations
```

# Available plugins

Image classification

  * [https://github.com/waikato-ufdl/wai-annotations-adams](https://github.com/waikato-ufdl/wai-annotations-adams)
  * [https://github.com/waikato-ufdl/wai-annotations-subdir](https://github.com/waikato-ufdl/wai-annotations-subdir)

Object detection

  * [https://github.com/waikato-ufdl/wai-annotations-adams](https://github.com/waikato-ufdl/wai-annotations-adams)
  * [https://github.com/waikato-ufdl/wai-annotations-coco](https://github.com/waikato-ufdl/wai-annotations-coco)
  * [https://github.com/waikato-ufdl/wai-annotations-opex](https://github.com/waikato-ufdl/wai-annotations-opex)
  * [https://github.com/waikato-ufdl/wai-annotations-roi](https://github.com/waikato-ufdl/wai-annotations-roi)
  * [https://github.com/waikato-ufdl/wai-annotations-tf](https://github.com/waikato-ufdl/wai-annotations-tf)
  * [https://github.com/waikato-ufdl/wai-annotations-vgg](https://github.com/waikato-ufdl/wai-annotations-vgg)
  * [https://github.com/waikato-ufdl/wai-annotations-voc](https://github.com/waikato-ufdl/wai-annotations-voc)
  * [https://github.com/waikato-ufdl/wai-annotations-yolo](https://github.com/waikato-ufdl/wai-annotations-yolo)
    
Image segmentation

  * [https://github.com/waikato-ufdl/wai-annotations-bluechannel](https://github.com/waikato-ufdl/wai-annotations-bluechannel)
  * [https://github.com/waikato-ufdl/wai-annotations-grayscale](https://github.com/waikato-ufdl/wai-annotations-grayscale)
  * [https://github.com/waikato-ufdl/wai-annotations-indexedpng](https://github.com/waikato-ufdl/wai-annotations-indexedpng)
  * [https://github.com/waikato-ufdl/wai-annotations-layersegments](https://github.com/waikato-ufdl/wai-annotations-layersegments)

Audio

  * [https://github.com/waikato-ufdl/wai-annotations-audio](https://github.com/waikato-ufdl/wai-annotations-audio)
  * [https://github.com/waikato-ufdl/wai-annotations-commonvoice](https://github.com/waikato-ufdl/wai-annotations-commonvoice)
  * [https://github.com/waikato-ufdl/wai-annotations-festvox](https://github.com/waikato-ufdl/wai-annotations-festvox)

Miscellaneous

  * [https://github.com/waikato-ufdl/wai-annotations-generic](https://github.com/waikato-ufdl/wai-annotations-generic) - generic plugins for wrapping user classes
  * [https://github.com/waikato-ufdl/wai-annotations-imgaug](https://github.com/waikato-ufdl/wai-annotations-imgaug) - image augmentation
  * [https://github.com/waikato-ufdl/wai-annotations-imgstats](https://github.com/waikato-ufdl/wai-annotations-imgstats) - image/label statistics
  * [https://github.com/waikato-ufdl/wai-annotations-imgvis](https://github.com/waikato-ufdl/wai-annotations-imgvis) - image visualization
  * [https://github.com/waikato-ufdl/wai-annotations-redis-predictions](https://github.com/waikato-ufdl/wai-annotations-redis-predictions) - making predictions via Redis backend
  * [https://github.com/waikato-ufdl/wai-annotations-video](https://github.com/waikato-ufdl/wai-annotations-video) - video support
