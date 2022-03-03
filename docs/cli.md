# CLI Support in wai-annotations

Command-line options are added to wai-annotations at the component level via the use of `Option` descriptor classes.
This allows for adding command-line options in a declarative style, specifying information about the nature and type of
the options, while letting wai-annotations automatically perform the work of getting information from the user and 
presenting it to the components at run-time.

To add an option to a component, create a class-level variable and assign an `Option` instance to it (see below for a
description of the available `Option` types). To read the value of an option as specified by the user, simply access
the class-level variable through the component instance e.g. `self.my_option` as if it were a property.

N.B. Although options are defined at the component level, wai-annotations aggregates them at the stage level. Therefore,
care must be taken not to use the same flag/s for multiple options, not only within a component (including its
ancestor classes), but also between components that are shared by a stage.

## Types of Options

### ClassOption

An option for selecting a Python class. Is initialised with a class-registry of the available choices the user can
select from. The user provides the name of a class in the registry and the class itself is returned.

### CountOption

Option which simply returns the number of times its flag was supplied to the command line. This is useful, for example,
for verbosity values, where increasing the number of flags increases the logging verbosity (e.g. `-vvv`). An
optional translation table can be provided which translates the actual value to some mapped value.

### FlagOption

A simple flag, which evaluates to True when provided on the command-line, or False if not (these semantics can be
inverted).

### TypedOption

The most versatile option, it takes a type to use to parse the command-line string/s provide by the user. Can return
a single-value of that type or a list of values of that type if set to take multiple arguments.

## Example

This example creates a processor component which takes a schedule of integers from the command line, and multiplies
incoming integers by the next integer in the schedule.

```python
# For typing the schedule
from typing import List

# The type of component we are making
from wai.annotations.core.component import ProcessorComponent  # or SourceComponent, or SinkComponent

# The type of option we want to add to our component
from wai.common.cli.options import TypedOption  # or ClassOption, or CountOption, or FlagOption

# We need some process-state to track where we are in the schedule. We output results as we get them, so no
# buffering occurs and therefore no finalisation is necessary
from wai.annotations.core.stream.util import ProcessState, RequiresNoFinalisation

# Type definitions for the streaming callbacks
from wai.annotations.core.stream import ThenFunction, DoneFunction


class MyProcessorComponent(
    RequiresNoFinalisation,
    ProcessorComponent[int, int]  # Processes integers into integers
):
    """
    My processor component, which multiplies incoming integers by values in a schedule, passed on the command-line.
    """
    # Where we are in the schedule. ProcessState takes an initialiser which is called before processing is started
    # to reset the state for each run. The initialiser takes the instance it is being used for, i.e. self. Here we
    # just initialise the index into the schedule to zero at the beginning of each run.
    schedule_index: int = ProcessState(lambda self: 0)
    
    # The option which defines the schedule.
    schedule: List[int] = TypedOption(
        "-s", "--schedule",  # The short and long flags to identify the option on the command-line
        type=int,  # The type that will be used to parse the command-line values
        action="concat",  # This flag can be specified multiple times, subsequent values will be appended to the list
        nargs="+",  # Means we can supply one or more values to this flag
        # choices=[...]  # If we wanted to allow choosing only from specific integers
        # default=[...]  # If we had a default schedule in mind. Omission means the default is the empty list
        required=True,  # We need a schedule, the empty list won't do!
        help="The schedule to multiply values by",  # Displayed to the user on usage
        metavar="INT"  # Displayed to the user on usage, describes the type of value that should be supplied
    )

    def process_element(
            self,
            element: int,
            then: ThenFunction[int],
            done: DoneFunction
    ):
        # Multiply the value by the current schedule value
        result = element * self.schedule[self.schedule_index]
        
        # Forward the calculated value
        then(result)
        
        # Move to the next position in the schedule
        self.schedule_index = (self.schedule_index + 1) % len(self.schedule)
    
```