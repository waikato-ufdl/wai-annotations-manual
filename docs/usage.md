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

### Dependencies

A number of libraries have their default logging set to `DEBUG`, which can output
unnecessary output in the console. wai.annotations sets the logging level for
some libraries to a higher level therefore. However, the user can adjust this again 
via environment variables, in case the logging output is required:

* h5py: `WAIANN_H5PY_LOGLEVEL` (default level: `WARNING`)
* matplotlib: `WAIANN_MATPLOTLIB_LOGLEVEL` (default level: `WARNING`)
* numba: `WAIANN_NUMBA_LOGLEVEL` (default level: `WARNING`)
* shapely: `WAIANN_SHAPELY_LOGLEVEL` (default level: `WARNING`)
* tensorflow: `WAIANN_TF_LOGLEVEL` (default level: `WARNING`)
