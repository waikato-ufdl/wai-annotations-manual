# How to use wai-annotations from the command-line

To convert a dataset using wai-annotations from the command-line, run the following command:

```
wai-annotations convert [CONVERSION OPTIONS] \
    input-type [INPUT OPTIONS] \
    [ISP/XDC [ISP/XDC OPTIONS]]... \
    output-type [OUTPUT OPTIONS]
```

(ISP=inline-stream-processor, XDC=cross-domain-conversion)

For the available conversion options, see [here](conversion_options.md).

To list of available plugins in your environment, run:

```
wai-annotations plugins
```

For the available domains in your environment, run:

```
wai-annotations domains
```

The `-h/--help` option can be given at any point in a command-string to provide the options available at
that point in the command.

Examples of how to run wai-annotations can be found [here](examples.md).
