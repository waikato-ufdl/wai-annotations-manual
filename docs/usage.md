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

Examples of how to run wai-annotations can be found [here](examples_overview.md).

## Logging

By default, all logging messages are being output. To change that, you can use the `WAIANN_LOG_LEVEL` environment 
variable, using one of the following levels (the higher the number the fewer messages):

* 10: DEBUG
* 20: INFO
* 30: WARNING
* 40: ERROR

### Numba logging

By default, numba's logging level gets set to `WARNING` to avoid deluge of debugging
messages. However, this can be changed via the `WAIANN_NUMBA_LOGLEVEL` environment
variable. Same levels are available as for `WAIANN_LOG_LEVEL`.
