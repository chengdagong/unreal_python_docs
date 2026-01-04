# unreal.RigUnit_SetScale

```python
class unreal.RigUnit_SetScale(execute_pin:RigVMExecutePin=\[\], item:RigElementKey=Ellipsis, space:RigVMTransformSpace=Ellipsis, initial:bool=False, scale:Vector=Ellipsis, weight:float=0.0, propagate_to_children:bool=False)
```


**Bases:** ``RigUnitMutable``


SetScale is used to set a single scale on hierarchy.

**C++ Source:**

- **Plugin**: ControlRig

- **Module**: ControlRig

- **File**: RigUnit\_SetTransform.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `execute_pin` (RigVMExecutePin): [Read-Write] \* This property is used to chain multiple mutable units together

- `initial` (bool): [Read-Write] Defines if the transform should be set as current (false) or initial (true).
Initial transforms for bones and other elements in the hierarchy represent the reference pose’s value.

- `item` (RigElementKey): [Read-Write] The item to set the scale for

- `propagate_to_children` (bool): [Read-Write] If set to true children of affected items in the hierarchy
will follow the transform change - otherwise only the parent will move.

- `scale` (Vector): [Read-Write] The new scale of the given item

- `space` (RigVMTransformSpace): [Read-Write] Defines if the scale should be set in local or global space

- `weight` (float): [Read-Write] Defines how much the change will be applied



---

_property_ `initial`: bool

[Read-Write] Defines if the transform should be set as current (false) or initial (true).
Initial transforms for bones and other elements in the hierarchy represent the reference pose’s value.

**Type:**

( bool)


---

_property_ `item`: RigElementKey

[Read-Write] The item to set the scale for

**Type:**

( RigElementKey)


---

_property_ `propagate_to_children`: bool

[Read-Write] If set to true children of affected items in the hierarchy
will follow the transform change - otherwise only the parent will move.

**Type:**

( bool)


---

_property_ `scale`: Vector

[Read-Write] The new scale of the given item

**Type:**

( Vector)


---

_property_ `space`: RigVMTransformSpace

[Read-Write] Defines if the scale should be set in local or global space

**Type:**

( RigVMTransformSpace)


---

_property_ `weight`: float

[Read-Write] Defines how much the change will be applied

**Type:**

( float)

### Table of Contents

- `unreal.RigUnit_SetScale`
  - `RigUnit_SetScale`
    - `RigUnit_SetScale.initial`
    - `RigUnit_SetScale.item`
    - `RigUnit_SetScale.propagate_to_children`
    - `RigUnit_SetScale.scale`
    - `RigUnit_SetScale.space`
    - `RigUnit_SetScale.weight`