# Architecture Overview

The wai-annotations architecture is made of a few layers:

- the stream layer
- the component layer
- the stage layer

## Stream Layer

The stream layer is the lowest-level stream-processing layer of the wai-annotations architecture.

See [here](stream.md) for a detailed description of the stream layer.

## Component Layer

The component layer is an extension to the stream layer, adding logging support and command-line parsing to each
of the source, processor and sink streaming base-classes. The resulting base-classes are SourceComponent,
ProcessorComponent, and SinkComponent.

To use logging for a component, simply call the `get_class_logger` method from a component class, or access the
`logger` property from a component instance.

See [here](cli.md) for a description of how to add command-line options to a component.

## Stage Layer

The stage layer groups partial-pipelines of components into conceptual "stages", where each stage represents an
operation at the dataset level in the pipeline. For example, the input stage of reading a dataset in some format might
involve a source component which parses valid filenames from the command-line, and passes them to a processor-component
which reads those files and passes on the actual file data.

Stages are specified by specifier classes (SourceStageSpecifier, ProcessorStageSpecifier, SinkStageSpecifier), which
provide the components used to create the stage, and also provide a description of the A.I. domains that the stage
can work with. For source/sink stages, a single domain is provided which defines the domain for which the component
can produce/consume datasets. For processor stages, a domain transfer-function is defined on the specifier, which
determines the output domain for a given input domain (or declares the input domain unusable with the processor stage).
wai-annotations uses the domain specifications to check that a series of stages is specified that will be able to pass
data from one stage to the next without error.

For information on how to create new processing stages, see [here](plugin.md)