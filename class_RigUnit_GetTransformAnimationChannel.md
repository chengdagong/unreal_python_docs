# unreal.RigUnit_GetTransformAnimationChannel

```python
class unreal.RigUnit_GetTransformAnimationChannel(control:Name='None', channel:Name='None', initial:bool=False, value:Transform=Ellipsis)
```


**Bases:** ``RigUnit_GetAnimationChannelBase``


Get Transform Channel is used to retrieve a control’s animation channel value

**C++ Source:**

- **Plugin**: ControlRig

- **Module**: ControlRig

- **File**: RigUnit\_ControlChannel.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `channel` (Name): [Read-Write] The name of the animation channel to retrieve the value for.

- `control` (Name): [Read-Write] The name of the Control to retrieve the value for.

- `initial` (bool): [Read-Write] If set to true the initial value will be returned

- `value` (Transform): [Read-Write] The current value of the animation channel



---

_property_ `value`: Transform

[Read-Only] The current value of the animation channel

**Type:**

( Transform)

### Table of Contents

- `unreal.RigUnit_GetTransformAnimationChannel`
  - `RigUnit_GetTransformAnimationChannel`
    - `RigUnit_GetTransformAnimationChannel.value`