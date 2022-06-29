# Adding components to wai-annotations through plugins

wai-annotations uses a plugin system to allow other libraries to add new processing stages
without modifying the base library source. This document details how to go about using this system.

## Generic wrappers

If you just want to run some code that won't ever make it into a released plugin, then you might 
want to make use of the [wai.annotations.generic](https://github.com/waikato-ufdl/wai-annotations-generic) 
module. This module provides wrappers around sources/ISPs/sinks, i.e., you only have to write the 
source/ISP/sink class itself but not all the other boiler plate code that will make your plugin 
available within the wai.annotations framework.

Check out the [example section](examples_generic.md). Also, the [wai.annotations.audio](https://github.com/waikato-ufdl/wai-annotations-audio)
module has a more [concrete example](examples_audio.md) for loading the [Urban8k](https://urbansounddataset.weebly.com/urbansound8k.html) 
audio dataset with this wrapper approach.


## Plugin Types

There are 3 types of stage which can be added to wai-annotations via plugin: input formats, processing stages and output
formats. New domains can also be added, but these are specified indirectly via any of the previous components.

## Domains

New domains are added indirectly to wai-annotations as dependencies of components, as a domain which has no components
is essentially unreachable to a conversion chain. However, the specification of new domains is treated as a
plugin-related issue, so it is detailed here.

Definition of a new domain is a multi-step process, as follows.

- Define the type of the (unannotated) data for the domain, as a sub-class of `Data`. Objects of this class hold the
  name and binary data for an instance, along with any additional meta-data.
- Define the type of the annotations for an instance in the domain. This can be any arbitrary type.
- Define the type of instances in the domain as a sub-class of `Instance`. This represents the association between
  a data-item and its annotations. At its simplest, this is just a container for the data-item and the annotations, but
  additional meta-data about the relation can be added for specific domains, if required.
- Define a specifier class for the domain, sub-classing `DomainSpecifier`. This advertises the domain to the
  wai-annotations framework.

### Example

```python
from typing import Type

# Import the base classes
from wai.annotations.core.domain import Data, Instance, DomainSpecifier

# Define the data-type which holds dataset item data
class MyDomainData(Data):
    @classmethod
    def from_file_data(cls, file_name: str, file_data: bytes) -> 'MyFileInfo':
        # If we don't need any additional information, or it is calculated in the init method
        return cls(file_name, file_data)
        
# Define the type of annotations for the domain
class MyDomainAnnotations:
    ...
    
# Define an instance type, adding additional functionality, if required
class MyDomainInstance(Instance[MyDomainData, MyDomainAnnotations]):
    @classmethod
    def data_type(cls) -> Type[MyDomainData]:
        return MyDomainData
    
    @classmethod
    def annotations_type(cls) -> Type[MyDomainAnnotations]:
        return MyDomainAnnotations
    
    def additional_method(self):
        ...

# Define the domain specifier reporting the various classes for domain instances
class MyDomainSpecifier(DomainSpecifier):
    @classmethod
    def domain_name(cls) -> str:
        return "my domain"
    
    @classmethod
    def description(cls) -> str:
        return "A detailed description of the domain"
    
    @classmethod
    def data_type(cls) -> Type[MyDomainData]:
        return MyDomainData
        
    @classmethod
    def annotations_type(cls) -> Type[MyDomainAnnotations]:
        return MyDomainAnnotations
        
    @classmethod
    def instance_class(cls) -> Type[MyDomainInstance]:
        return MyDomainInstance
```

## Stages

Stages are a partial pipeline of components. Input stages consist of a source component and zero or more processing
components, processing stages only consist of processing components, and output stages consist of zero or more
processing components followed by a sink component.

To create a new stage, the individual components must be created and then advertised through a stage specifier class. 
The base classes for components can be imported from wai-annotations' core package:

```python
from wai.annotations.core.component import SourceComponent
from wai.annotations.core.component import ProcessorComponent
from wai.annotations.core.component import SinkComponent
```

Sub-class the base classes for the types of components you are trying to implement, and fill in the generic
type-parameters and abstract methods. See the examples below for guidance.

Then sub-class one of the stage-specifier classes for the type of stage you are creating:

```python
from wai.annotations.core.specifier import SourceStageSpecifier
from wai.annotations.core.specifier import ProcessorStageSpecifier
from wai.annotations.core.specifier import SinkStageSpecifier
```

The specifier classes require that you override the `description` method, which provides a description of the stage,
and the `components` method, which lists the components which comprise the stage. Source/Sink stages also require a
`domain` method, which returns the domain that the stage reads/writes. Processor stages instead have a 
`domain_transfer_function` method, which returns the output domain for a given input domain (this way, processing
stages can be used in multiple domains).

In order for wai-annotations to recognise your plugin, the specifier class needs to be advertised as an entry point in
your setup script under the `wai.annotations.plugins` group:

```python
# setup.py
from setuptools import setup

setup(
    ...,
    entry_points={
        "wai.annotations.plugins": [
            # Input stage
            "from-my-input-format=com.example.specifiers:MySourceStageSpecifier",
            
            # Output stage
            "to-my-output-format=com.example.specifiers:MySinkStagepecifier",

            # Processor stages
            "my-processor=com.example.specifiers:MyProcessorStageSpecifier"
        ]
    }
)
```

### Example Input Stage

Input stages consist of a source component followed by zero or more processing components. Typically the source
component will be `wai.annotations.core.component.util.LocalFilenameSource`, but this is not required. What is
required is that the final component of the stage outputs instances in the domain that the stage operates.

```python
from typing import Type, Tuple

from wai.annotations.core.component import SourceComponent, ProcessorComponent
from wai.annotations.domain.image.object_detection import (
  ImageObjectDetectionInstance, ImageObjectDetectionDomainSpecifier
)
from wai.annotations.core.specifier import SourceStageSpecifier
from wai.annotations.core.stream import ThenFunction, DoneFunction

# Define the source component (generic type is the type this source produces)
class MySourceComponent(SourceComponent[str]):
  # Any command-line options here...

  def produce(
          self,
          then: ThenFunction[str],
          done: DoneFunction
  ):
    # Call then(str) multiple times...
    ...

    # Call done()
    done()


# Define a processor component to parse each string from the source component into a domain instance
# (generic types are input and output type respectively)
class MyProcessorComponent(ProcessorComponent[str, ImageObjectDetectionInstance]):
  # Any command-line options here...

  def process_element(
          self,
          element: str,
          then: ThenFunction[ImageObjectDetectionInstance],
          done: DoneFunction
  ):
    # Parse each string and forward
    then(self._parse(element))

  def finish(
          self,
          then: ThenFunction[ImageObjectDetectionInstance],
          done: DoneFunction
  ):
    # Perform any clean-up
    ...

    # Call done
    done()

  def _parse(self, element: str) -> ImageObjectDetectionInstance:
    # Parse the string into an instance
    ...

# Create the specifier class for the stage
class MySourceStageSpecifier(SourceStageSpecifier):
  @classmethod
  def description(cls) -> str:
    return "My source stage"

  @classmethod
  def components(cls) -> Tuple[Type[MySourceComponent], Type[MyProcessorComponent]]:
    return MySourceComponent, MyProcessorComponent

  @classmethod
  def domain(cls) -> Type[ImageObjectDetectionDomainSpecifier]:
    return ImageObjectDetectionDomainSpecifier
```

### Example Output Stage

Output stages consist of zero or more processing components followed by a single sink component. The first component of
the stage must take instances in the stage's domain as input.

```python
from typing import Type, Tuple

from wai.annotations.core.component import ProcessorComponent, SinkComponent
from wai.annotations.domain.image.object_detection import (
    ImageObjectDetectionInstance, ImageObjectDetectionDomainSpecifier
)
from wai.annotations.core.specifier import SinkStageSpecifier
from wai.annotations.core.stream import ThenFunction, DoneFunction
        
# Define a processor component to format each domain instance into a string
# (generic types are input and output type respectively)
class MyProcessorComponent(ProcessorComponent[ImageObjectDetectionInstance, str]):
    # Any command-line options here...

    def process_element(
            self,
            element: ImageObjectDetectionInstance,
            then: ThenFunction[str],
            done: DoneFunction
    ):
        # Format each instance and forward
        then(self._format(element))
        
    def finish(
            self,
            then: ThenFunction[ImageObjectDetectionInstance],
            done: DoneFunction
    ):
        # Perform any clean-up
        ...
    
        # Call done
        done()
        
    def _format(self, element: ImageObjectDetectionInstance) -> str:
        # Format the instance into an str
        ...

# Define the sink component (generic type is the type this sink consumes)
class MySinkComponent(SinkComponent[str]):
  # Any command-line options here...

  def consume_element(self, element: str):
    # E.g. write the string to disk
    ...

  def finish(self):
    # Any tidy-up
    ...

# Create the specifier class for the stage
class MySinkStageSpecifier(SinkStageSpecifier):
    @classmethod
    def description(cls) -> str:
        return "My source stage"
    
    @classmethod
    def components(cls) -> Tuple[Type[MyProcessorComponent], Type[MySinkComponent]]:
        return  MyProcessorComponent, MySinkComponent
    
    @classmethod
    def domain(cls) -> Type[ImageObjectDetectionDomainSpecifier]:
        return ImageObjectDetectionDomainSpecifier
```

### Example Processor Stage

Processor stages consist of one or more processing components. The domain-transfer function defined on the specifier
must match the input/output types of the chain of components for the stage.

```python
from typing import Type, Tuple

from wai.annotations.core.component import ProcessorComponent
from wai.annotations.core.domain import Instance, DomainSpecifier
from wai.annotations.core.specifier import ProcessorStageSpecifier
from wai.annotations.core.stream import ThenFunction, DoneFunction
from wai.annotations.core.stream.util import ProcessState
        
# Define a processor component to remove every second instance (for any domain)
# (generic types are input and output type respectively)
class MyProcessorComponent(ProcessorComponent[Instance, Instance]):
    # Any command-line options here...
    
    # Process-state to track whether we need to remove the next instance
    remove_next: bool = ProcessState(lambda self: False)

    def process_element(
            self,
            element: Instance,
            then: ThenFunction[Instance],
            done: DoneFunction
    ):
        if not self.remove_next:
            then(element)
        
        self.remove_next = not self.remove_next
        
    def finish(
            self,
            then: ThenFunction[Instance],
            done: DoneFunction
    ):
        # Perform any clean-up
        ...
    
        # Call done
        done()

# Create the specifier class for the stage
class MyProcessorStageSpecifier(ProcessorStageSpecifier):
    @classmethod
    def description(cls) -> str:
        return "My source stage"
    
    @classmethod
    def components(cls) -> Tuple[Type[MyProcessorComponent]]:
        return MyProcessorComponent,
    
    @classmethod
    def domain_transfer_function(
            cls,
            input_domain: Type[DomainSpecifier]
    ) -> Type[DomainSpecifier]:
        # Because our processor stage works in any domain, and does not cross domains, just return the input domain
        return input_domain
```

### Best Practice

Although in each of the examples shown here, we have defined our plugin specifiers in the same file as the components
they advertise, this is not the recommended approach. The specifier types should instead be defined in their own
sub-package, and the methods should locally import the specified types (instead of globally at the beginning of the
specifier Python file). This is so the specifier can be imported into the plugin system without importing potentially
heavy-weight libraries that the components depend on for their functionality. This way the system can provide reflection
of the available plugins, but only load those plugins that are actually selected for use in a conversion.

## Adding Command-Line Options to Plugin Components

See [here](cli.md) for a description of command-line option support in wai-annotations.

## Splitting

Sink-components (and by extension sink-stages) may require that the incoming instances be split across a number of
output locations. Special support for splitting is provided in the `wai.annotations.core.component.util` sub-package.
See [here](component_util.md#Splitting) for information on how to add splitting to your sink-stages.
