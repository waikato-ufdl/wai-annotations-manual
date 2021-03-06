# Welcome to wai-annotations

wai-annotations is a Python library for converting annotation datasets between various annotation formats 
of data domains such as images and audio. With its command-line tools, you can, e.g., create conversion 
pipelines or split dataset batches into subsets.

The library also offers plugins for reading/writing videos, preprocessing data, for generating statistics 
and visualizations, as well as incorporating predictions made via a Redis backend (e.g., using deep 
learning models).

* [Installation](install.md) - how to install the library
* [Usage](usage.md) - running the library from the command-line
* [Examples](examples_overview.md) - common use-cases
* [Docker](docker.md) - using wai.annotations via pre-built docker images
* [Architecture overview](architecture_overview.md) - description of the internals 
* [Plugin Guide](plugin.md) - adding new domains/formats/conversions
* [Domains](domains.md) - supported domains
* [Plugins](plugins.md) - available plugins
* [Glossary](glossary.md) - explanations of terms

wai.annotations is being developed as part of the [User-friendly Deep Learning](https://ufdl.cms.waikato.ac.nz/) project.
