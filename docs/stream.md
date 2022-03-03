# Stream Layer

The stream layer provides classes for creating custom stream-processing pipelines. Each pipeline consists of: a source,
which injects items into the pipeline for processing; processors, which take items and process them; and a sink, which
consumes the items coming out of the pipeline.

There are 3 base-classes representing sources, processors and sinks (respectively: StreamSource, StreamProcessor and
StreamSink). These classes should be inherited to provide customised stream-processing functionality. The Pipeline class
gathers the individual stream elements into a whole, connects each element to the previous and next elements, and
ensures that the elements follow the pipeline's calling semantics (see below).

Note that while the stream-processing elements are typed on the items they consume/produce, this is only for linting
purposes and not enforced at run-time.

## Calling semantics

For sources and processors, the ability to pass items on to later elements in the processing pipeline is provided
through 2 callback functions, `then` and `done`. `then` forwards an item to the next element of the pipeline, and
`done` signals that no more items will be forwarded. This design was chosen over e.g. iterators as it ensures that when
an error occurs, the relevant information which led to the error is retained on the call-stack. This is a useful aid
for debugging.

However, this does mean that the potential exists for the callbacks to called in an arbitrary order, when only
certain permutations are sensible. The intended calling semantics of the 2 callbacks are: 0 or more calls to `then`
to forward items, followed by exactly 1 call to `done` to signal termination.

The pipeline class constructs these callbacks so that, if they are not called in the correct order, an error occurs.
Specifically, calling `then` after `done` has been called will raise an error, as will not calling `done` at all. In
practice, `done` is written to be idempotent, such that calling it multiple times is the same as calling it once.

## StreamSource

Stream sources should implement the `produce` method to inject items into the pipeline. The method should call the 
`then` callback with each item to inject as its argument. Once all items have been produced, the source should then
call the `done` callback.

## StreamProcessor

Stream processors should implement `process_element` method to receive items from the previous processing-element in
the pipeline for processing. They should also implement the `finish` method to finalise processing after all items
have been received.

Both methods take the `then` and `done` callbacks as arguments, so processors can process items and forward the
processed results as they arrive, or batch them and perform processing/forwarding in bulk.

An optional `start` method is available, which can be overridden to perform any set-up required before the processor
starts receiving items.

## StreamSink

Stream sinks should implement the `consume_element` method to consume items produced by the pipeline. They should also
implement the `finish` method to perform any tidy-up once the pipeline has terminated.

An optional `start` method is available, which can be overridden to perform any set-up required before the sink
starts receiving items.

## Pipeline

The Pipeline class take an optional source, zero or more processors, and an optional sink as its constructor arguments.
When the `process` method is called, the processing elements are connected together, the `start` methods for each
processor and the sink are called, and the source is instructed to start producing items. Optionally, an iterable can
be passed to the `process` method to replace the pipeline's own source, and/or a function can be passed to replace
the pipeline's sink.

When the pipeline is connecting the processing elements together, it also inserts checks for the calling semantics,
which will raise an exception if they are not adhered to.

## Utilities

### RequiresNoFinalisation

Mixin class that can be used with StreamProcessor/StreamSink to automatically implement the `finish` method. It will
call the `done` callback automatically for processors if it has not been called already.

### ProcessState

Descriptor class which adds per-stream state to a stream-processing element. Takes an initialiser function as its only
constructor argument. The initialiser is used to re-initialise the state before each stream is processed by the
pipeline that contains the element. The state can be modified during stream processing to track per-stream state, but
the changes are discarded once a new stream is processed.
