# unreal.RigUnit_GetTransformAnimationChannelFromItem

```python
class unreal.RigUnit_GetTransformAnimationChannelFromItem(item:RigElementKey=Ellipsis, initial:bool=False, value:Transform=Ellipsis)
```


**Bases:** ``RigUnit_GetAnimationChannelFromItemBase``


Get Transform Channel is used to retrieve a control’s animation channel value

**C++ Source:**

- **Plugin**: ControlRig

- **Module**: ControlRig

- **File**: RigUnit\_ControlChannelFromItem.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `initial` (bool): [Read-Write] If set to true the initial value will be returned

- `item` (RigElementKey): [Read-Write] The item representing the channel

- `value` (Transform): [Read-Write] The current value of the animation channel



---

_property_ `value`: Transform

[Read-Only] The current value of the animation channel

**Type:**

( Transform)

### Table of Contents

- `unreal.RigUnit_GetTransformAnimationChannelFromItem`
  - `RigUnit_GetTransformAnimationChannelFromItem`
    - `RigUnit_GetTransformAnimationChannelFromItem.value`