# unreal.AutomationScheduler

```python
class unreal.AutomationScheduler
```


**Bases:** ``object``


Used to schedule python functions and generators to be run between editor ticks.
One iteration of a generator is done per tick. It means that each yield statement will call for an editor tick.
If a function or yield statement returns a function or a generator, that object is scheduled right after the next
tick. The previously scheduled tasks are run afterwards.

_classmethod_ add\_latent\_command( _task_)

Add a function or a generator to the AutomationScheduler schedule.
Can be used as a decorator to add a function.
Note that order sequence is important here. Registered first is run first.

ie:

@unreal.AutomationScheduler.add\_latent\_command
def setup\_level():

> pass

_classmethod_ cleanup()

Force a shutdown of the singleton instance if any is running

schedule _=None_

Scheduled tasks as a priority list. It is None if the scheduler was not initiated.

_classmethod_ set\_latent\_command\_timeout( _seconds_)

Set the Python Automation Test latent command timeout in second

### Table of Contents

- `unreal.AutomationScheduler`
  - `AutomationScheduler`
    - `AutomationScheduler.add_latent_command()`
    - `AutomationScheduler.cleanup()`
    - `AutomationScheduler.schedule`
    - `AutomationScheduler.set_latent_command_timeout()`