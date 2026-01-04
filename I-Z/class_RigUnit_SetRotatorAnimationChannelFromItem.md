# unreal.RigUnit_SetRotatorAnimationChannelFromItem

```python
class unreal.RigUnit_SetRotatorAnimationChannelFromItem(item:RigElementKey=Ellipsis, initial:bool=False, execute_pin:RigVMExecutePin=\[\], value:Rotator=Ellipsis)
```


**Bases:** ``RigUnit_SetAnimationChannelBaseFromItem``


Set Rotator Channel is used to set a control’s animation channel value

**C++ Source:**

- **Plugin**: ControlRig

- **Module**: ControlRig

- **File**: RigUnit\_ControlChannelFromItem.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `execute_pin` (RigVMExecutePin): [Read-Write]

- `initial` (bool): [Read-Write] If set to true the initial value will be returned

- `item` (RigElementKey): [Read-Write] The item representing the channel

- `value` (Rotator): [Read-Write] The new value of the animation channel



---

_property_ `value`: Rotator

[Read-Write] The new value of the animation channel

**Type:**

( Rotator)

### Table of Contents

- `unreal.RigUnit_SetRotatorAnimationChannelFromItem`
  - `RigUnit_SetRotatorAnimationChannelFromItem`
    - `RigUnit_SetRotatorAnimationChannelFromItem.value`