# unreal.RigUnit_GetTransform

```python
class unreal.RigUnit_GetTransform(item:RigElementKey=Ellipsis, space:RigVMTransformSpace=Ellipsis, initial:bool=False, transform:Transform=Ellipsis)
```


**Bases:** ``RigUnit``


GetTransform is used to retrieve a single transform from a hierarchy.

**C++ Source:**

- **Plugin**: ControlRig

- **Module**: ControlRig

- **File**: RigUnit\_GetTransform.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `initial` (bool): [Read-Write] Defines if the transform should be retrieved as current (false) or initial (true).
Initial transforms for bones and other elements in the hierarchy represent the reference pose’s value.

- `item` (RigElementKey): [Read-Write] The item to retrieve the transform for

- `space` (RigVMTransformSpace): [Read-Write] Defines if the transform should be retrieved in local or global space

- `transform` (Transform): [Read-Write] The current transform of the given item - or identity in case it wasn’t found.



---

_property_ `initial`: bool

[Read-Write] Defines if the transform should be retrieved as current (false) or initial (true).
Initial transforms for bones and other elements in the hierarchy represent the reference pose’s value.

**Type:**

( bool)


---

_property_ `item`: RigElementKey

[Read-Write] The item to retrieve the transform for

**Type:**

( RigElementKey)


---

_property_ `space`: RigVMTransformSpace

[Read-Write] Defines if the transform should be retrieved in local or global space

**Type:**

( RigVMTransformSpace)


---

_property_ `transform`: Transform

[Read-Only] The current transform of the given item - or identity in case it wasn’t found.

**Type:**

( Transform)

### Table of Contents

- `unreal.RigUnit_GetTransform`
  - `RigUnit_GetTransform`
    - `RigUnit_GetTransform.initial`
    - `RigUnit_GetTransform.item`
    - `RigUnit_GetTransform.space`
    - `RigUnit_GetTransform.transform`