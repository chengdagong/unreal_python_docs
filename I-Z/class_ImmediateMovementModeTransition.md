# unreal.ImmediateMovementModeTransition

```python
class unreal.ImmediateMovementModeTransition(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``BaseMovementModeTransition``


Simple transition that evaluates true if a “next mode” is set. Used internally only by the Mover plugin.

**C++ Source:**

- **Plugin**: Mover

- **Module**: Mover

- **File**: MovementModeTransition.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `allow_mode_reentry` (bool): [Read-Write] Whether this transition should reenter a mode if it evaluates true and wants to transition into a mode the actor is already in

- `first_sub_step_only` (bool): [Read-Write] Whether this transition should only apply to the first step of the update. If true, modes reached after transitions or mode changes
in the current update will not consider this transition

- `shared_settings_classes` (Array[type(Class)]): [Read-Write] Settings object type that this mode depends on. May be shared with other transitions and movement modes. When the transition is added to a Mover Component, it will create a shared instance of this settings class.

- `supports_async` (bool): [Read-Write] Whether this movement mode transition supports being part of an asynchronous movement simulation (running concurrently with the gameplay thread)
Specifically for the Evaluate and Trigger functions


### Table of Contents

- `unreal.ImmediateMovementModeTransition`
  - `ImmediateMovementModeTransition`