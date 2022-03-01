# Installation of wai-annotations

To install wai-annotations issue the following commands using pip:

```commandline
pip install wai.annotations.core
```

`wai-annotations-core` does not come with any input/output formats installed. You will need to install a plugin for each
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
  * [https://github.com/waikato-ufdl/wai-annotations-roi](https://github.com/waikato-ufdl/wai-annotations-roi)
  * [https://github.com/waikato-ufdl/wai-annotations-tf](https://github.com/waikato-ufdl/wai-annotations-tf)
  * [https://github.com/waikato-ufdl/wai-annotations-vgg](https://github.com/waikato-ufdl/wai-annotations-vgg)
  * [https://github.com/waikato-ufdl/wai-annotations-voc](https://github.com/waikato-ufdl/wai-annotations-voc)
  * [https://github.com/waikato-ufdl/wai-annotations-yolo](https://github.com/waikato-ufdl/wai-annotations-yolo)
    
Image segmentation

  * [https://github.com/waikato-ufdl/wai-annotations-bluechannel](https://github.com/waikato-ufdl/wai-annotations-bluechannel)
  * [https://github.com/waikato-ufdl/wai-annotations-indexedpng](https://github.com/waikato-ufdl/wai-annotations-indexedpng)
  * [https://github.com/waikato-ufdl/wai-annotations-layersegments](https://github.com/waikato-ufdl/wai-annotations-layersegments)

Audio

  * [https://github.com/waikato-ufdl/wai-annotations-commonvoice](https://github.com/waikato-ufdl/wai-annotations-commonvoice)
  * [https://github.com/waikato-ufdl/wai-annotations-festvox](https://github.com/waikato-ufdl/wai-annotations-festvox)

Image augmentation

  * [https://github.com/waikato-ufdl/wai-annotations-imgaug](https://github.com/waikato-ufdl/wai-annotations-imgaug)
