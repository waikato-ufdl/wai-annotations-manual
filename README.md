# wai-annotations-manual

Manual for the wai-annotations library for converting various annotation formats
into each other.

You can view the auto-generated documentation here:

https://ufdl.cms.waikato.ac.nz/wai-annotations-manual/


## Installation

*mkdocs* works with Python 2.7 and 3.x.

Best approach is to install mkdocs (>= 1.1.0) in a virtual environment 
(`venv` directory):

* Python 3

  ```
  virtualenv -p /usr/bin/python3 venv
  ```

* Install the mkdocs package

  ```
  ./venv/bin/pip install mkdocs==1.4.2 mkdocs-video==1.3.0 jinja2==3.1.2 "Markdown<3.4.0" mkdocs-material==8.5.10
  ```


## Content

In order for content to show up, it needs to be added to the configuration, 
i.e., in the `pages` section of the `mkdocs.yml` file.

Some pointers:

* [Images and media](http://www.mkdocs.org/user-guide/writing-your-docs/#images-and-media)
* [Linking](http://www.mkdocs.org/user-guide/writing-your-docs/#linking-documents)
* [mkdocs.yml](http://www.mkdocs.org/user-guide/configuration/)


## Build

[mkdocs](http://www.mkdocs.org/) is used to generate HTML from the 
markdown documents and images:

```
./venv/bin/mkdocs build --clean
```


## Testing

You can test what the site looks like, using the following command
and opening a browser on [localhost:8000](http://127.0.0.1:8000):

mkdocs monitors setup and markdown files, so you can just add and edit
them as you like, it will automatically rebuild and refresh the browser.

```
./venv/bin/mkdocs build --clean && ./venv/bin/mkdocs serve
```


## Manual deployment

The website gets automatically generated through Github actions. However, you
can manually deploy the current state to Github pages with the following command:

```
./venv/bin/mkdocs gh-deploy --clean
```

## Updating plugin documentation

After a new wai.annotations release, update the plugins page:

* Create a new virtual environment

  ```commandline
  virtualenv -p /usr/bin/python3 venv
  ```

* Install wai.annotations

  ```commandline
  ./venv/bin/pip install wai.annotations
  ```

* Update the [doc/plugins.md](doc/plugins.md) file with the following command:

  ```commandline
  ./venv/bin/wai-annotations plugins -f markdown -g > docs/plugins.md
  ```

* Clean up any logging output that the start of the generated file before committing it
