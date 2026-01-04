# unreal.RigUnit_GetVector2DAnimationChannel

```python
class unreal.RigUnit_GetVector2DAnimationChannel(control:Name='None', channel:Name='None', initial:bool=False, value:Vector2D=Ellipsis)
```


**Bases:** ``RigUnit_GetAnimationChannelBase``


Get Vector2D Channel is used to retrieve a control’s animation channel value

**C++ Source:**

- **Plugin**: ControlRig

- **Module**: ControlRig

- **File**: RigUnit\_ControlChannel.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `channel` (Name): [Read-Write] The name of the animation channel to retrieve the value for.

- `control` (Name): [Read-Write] The name of the Control to retrieve the value for.

- `initial` (bool): [Read-Write] If set to true the initial value will be returned

- `value` (Vector2D): [Read-Write] The current value of the animation channel



---

_property_ `value`: Vector2D

[Read-Only] The current value of the animation channel

**Type:**

( Vector2D)

### Table of Contents

- `unreal.RigUnit_GetVector2DAnimationChannel`
  - `RigUnit_GetVector2DAnimationChannel`
    - `RigUnit_GetVector2DAnimationChannel.value`