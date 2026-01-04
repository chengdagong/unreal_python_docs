# unreal.RigUnit_SetRotation

```python
class unreal.RigUnit_SetRotation(execute_pin:RigVMExecutePin=\[\], item:RigElementKey=Ellipsis, space:RigVMTransformSpace=Ellipsis, initial:bool=False, value:Quat=Ellipsis, weight:float=0.0, propagate_to_children:bool=False)
```


**Bases:** ``RigUnitMutable``


SetRotation is used to set a single rotation on hierarchy.

**C++ Source:**

- **Plugin**: ControlRig

- **Module**: ControlRig

- **File**: RigUnit\_SetTransform.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `execute_pin` (RigVMExecutePin): [Read-Write] \* This property is used to chain multiple mutable units together

- `initial` (bool): [Read-Write] Defines if the transform should be set as current (false) or initial (true).
Initial transforms for bones and other elements in the hierarchy represent the reference pose’s value.

- `item` (RigElementKey): [Read-Write] The item to set the rotation for

- `propagate_to_children` (bool): [Read-Write] If set to true children of affected items in the hierarchy
will follow the transform change - otherwise only the parent will move.

- `space` (RigVMTransformSpace): [Read-Write] Defines if the rotation should be set in local or global space

- `value` (Quat): [Read-Write] The new rotation of the given item

- `weight` (float): [Read-Write] Defines how much the change will be applied



---

_property_ `initial`: bool

[Read-Write] Defines if the transform should be set as current (false) or initial (true).
Initial transforms for bones and other elements in the hierarchy represent the reference pose’s value.

**Type:**

( bool)


---

_property_ `item`: RigElementKey

[Read-Write] The item to set the rotation for

**Type:**

( RigElementKey)


---

_property_ `propagate_to_children`: bool

[Read-Write] If set to true children of affected items in the hierarchy
will follow the transform change - otherwise only the parent will move.

**Type:**

( bool)


---

_property_ `rotation`: Quat

‘rotation’ was renamed to ‘value’.

**Type:**

deprecated


---

_property_ `space`: RigVMTransformSpace

[Read-Write] Defines if the rotation should be set in local or global space

**Type:**

( RigVMTransformSpace)


---

_property_ `value`: Quat

[Read-Write] The new rotation of the given item

**Type:**

( Quat)


---

_property_ `weight`: float

[Read-Write] Defines how much the change will be applied

**Type:**

( float)

### Table of Contents

- `unreal.RigUnit_SetRotation`
  - `RigUnit_SetRotation`
    - `RigUnit_SetRotation.initial`
    - `RigUnit_SetRotation.item`
    - `RigUnit_SetRotation.propagate_to_children`
    - `RigUnit_SetRotation.rotation`
    - `RigUnit_SetRotation.space`
    - `RigUnit_SetRotation.value`
    - `RigUnit_SetRotation.weight`