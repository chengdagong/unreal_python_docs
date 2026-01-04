# unreal.RigUnit_GetIntAnimationChannel

```python
class unreal.RigUnit_GetIntAnimationChannel(control:Name='None', channel:Name='None', initial:bool=False, value:int=0)
```


**Bases:** ``RigUnit_GetAnimationChannelBase``


Get Int Channel is used to retrieve a control’s animation channel value

**C++ Source:**

- **Plugin**: ControlRig

- **Module**: ControlRig

- **File**: RigUnit\_ControlChannel.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `channel` (Name): [Read-Write] The name of the animation channel to retrieve the value for.

- `control` (Name): [Read-Write] The name of the Control to retrieve the value for.

- `initial` (bool): [Read-Write] If set to true the initial value will be returned

- `value` (int32): [Read-Write] The current value of the animation channel



---

_property_ `value`: int

[Read-Only] The current value of the animation channel

**Type:**

(int32)

### Table of Contents

- `unreal.RigUnit_GetIntAnimationChannel`
  - `RigUnit_GetIntAnimationChannel`
    - `RigUnit_GetIntAnimationChannel.value`