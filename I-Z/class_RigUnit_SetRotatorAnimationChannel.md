# unreal.RigUnit_SetRotatorAnimationChannel

```python
class unreal.RigUnit_SetRotatorAnimationChannel(control:Name='None', channel:Name='None', initial:bool=False, execute_pin:RigVMExecutePin=\[\], value:Rotator=Ellipsis)
```


**Bases:** ``RigUnit_SetAnimationChannelBase``


Set Rotator Channel is used to set a control’s animation channel value

**C++ Source:**

- **Plugin**: ControlRig

- **Module**: ControlRig

- **File**: RigUnit\_ControlChannel.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `channel` (Name): [Read-Write] The name of the animation channel to retrieve the value for.

- `control` (Name): [Read-Write] The name of the Control to retrieve the value for.

- `execute_pin` (RigVMExecutePin): [Read-Write]

- `initial` (bool): [Read-Write] If set to true the initial value will be returned

- `value` (Rotator): [Read-Write] The new value of the animation channel



---

_property_ `value`: Rotator

[Read-Write] The new value of the animation channel

**Type:**

( Rotator)

### Table of Contents

- `unreal.RigUnit_SetRotatorAnimationChannel`
  - `RigUnit_SetRotatorAnimationChannel`
    - `RigUnit_SetRotatorAnimationChannel.value`