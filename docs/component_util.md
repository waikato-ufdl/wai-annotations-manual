# Utility Components

wai-annotations comes with some utility base-classes for common types of components, found in the
`wai.annotations.core.component.util` package. They are listed here.

## Input

### LocalFilenameSource

TODO

### AnnotationFileProcessor

TODO

## Output

### LocalFileWriter

TODO

### SeparateFileWriter

TODO

### JSONFileWriter

TODO

## Splitting

### SplitSink

Specialised sink component for handling splitting the stream of processed items among a group of splits. Takes 2
options: `--split-names`, followed by a name for each split; and `--split-ratios`, followed by an integer ratio of
how many items to add to each split. The sink component will then alternate which split it is acting on behalf of for
each item it receives. The alternation is designed so that at any stage, the ratio of items processed for each split is
as close as possible to the specified `--split-ratios`.

Sub-classes of `SplitSink` should implement the `consume_element_for_split`/`finish_split` methods, similar to an
ordinary sink component. During execution of either of these methods, the following information can be utilised:

- `self.is_splitting`: whether the user specified any splits to perform.
- `self.split_label`: the label of the current split (specified by `--split-names`). This is `None` if splits weren't
  specified.

The following sections detail additional functionality that can be added to split-sinks.

### SplitState

Specialised form of [process state](stream.md#ProcessState) which manages separate state for each split. Accessing this
property will return a separate instance depending on which split the component is currently acting for.

### RequiresNoSplitFinalisation

Specialised form of [the RequiresNoFinalisation mixin](stream.md#RequiresNoFinalisation), which declares that the
split-sink doesn't need to perform any clean-up after all items have been processed. This automatically implements
`finish_split`.

### WithPersistentSplitFiles

A mixin class for use with components which inherit from `SplitSink` and need to keep files open while writing them
across the splits. The `_init_split_files` method should be implemented to open all files needed by the sink, and return
them as some sort of collection. The `_iterate_split_files` should iterate over the collection returned by
`_init_split_files`. Components which implement this mixin can then access the `_split_files` property during
execution of their `consume_element_for_split`/`finish_split` methods to get access to the file-collection for the
current split.

## Other

General-purpose utilities for components.

### Buffer

This processor component buffers the entire stream, and passes it as a list to the next component in its `finish`
method.

### Enumerator

This processor component enumerates each item passed to it, forwarding a tuple of the 0-based index of the item and
the item itself.

### WithRandomness

This is a mixin class which can be used with any component, and adds a `--seed` option for randomisation. The help-text
for the option can be specified. If the user sets a seed value, the `random` property will provide a `Random` instance
initialised with the provided seed. If the option was not set, `None` will be returned by the property.