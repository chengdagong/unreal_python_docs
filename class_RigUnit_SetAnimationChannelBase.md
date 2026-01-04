# unreal.RigUnit_SetAnimationChannelBase

```python
class unreal.RigUnit_SetAnimationChannelBase(control:Name='None', channel:Name='None', initial:bool=False, execute_pin:RigVMExecutePin=\[\])
```


**Bases:** ``RigUnit_GetAnimationChannelBase``


Set Animation Channel is used to change a control’s animation channel value

**C++ Source:**

- **Plugin**: ControlRig

- **Module**: ControlRig

- **File**: RigUnit\_ControlChannel.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `channel` (Name): [Read-Write] The name of the animation channel to retrieve the value for.

- `control` (Name): [Read-Write] The name of the Control to retrieve the value for.

- `execute_pin` (RigVMExecutePin): [Read-Write]

- `initial` (bool): [Read-Write] If set to true the initial value will be returned



---

_property_ `execute_pin`: RigVMExecutePin

[Read-Write]

**Type:**

( RigVMExecutePin)

### Table of Contents

- `unreal.RigUnit_SetAnimationChannelBase`
  - `RigUnit_SetAnimationChannelBase`
    - `RigUnit_SetAnimationChannelBase.execute_pin`