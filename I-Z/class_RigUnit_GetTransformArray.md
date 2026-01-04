# unreal.RigUnit_GetTransformArray

```python
class unreal.RigUnit_GetTransformArray(items:RigElementKeyCollection=Ellipsis, space:RigVMTransformSpace=Ellipsis, initial:bool=False, transforms:None=\[\])
```


**Bases:** ``RigUnit``


GetTransformArray is used to retrieve an array of transforms from the hierarchy.

**C++ Source:**

- **Plugin**: ControlRig

- **Module**: ControlRig

- **File**: RigUnit\_GetTransform.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `initial` (bool): [Read-Write] Defines if the transforms should be retrieved as current (false) or initial (true).
Initial transforms for bones and other elements in the hierarchy represent the reference pose’s value.

- `items` (RigElementKeyCollection): [Read-Write] The items to retrieve the transforms for

- `space` (RigVMTransformSpace): [Read-Write] Defines if the transforms should be retrieved in local or global space

- `transforms` (Array[Transform]): [Read-Write] The current transform of the given item - or identity in case it wasn’t found.



---

_property_ `initial`: bool

[Read-Write] Defines if the transforms should be retrieved as current (false) or initial (true).
Initial transforms for bones and other elements in the hierarchy represent the reference pose’s value.

**Type:**

( bool)


---

_property_ `items`: RigElementKeyCollection

[Read-Write] The items to retrieve the transforms for

**Type:**

( RigElementKeyCollection)


---

_property_ `space`: RigVMTransformSpace

[Read-Write] Defines if the transforms should be retrieved in local or global space

**Type:**

( RigVMTransformSpace)


---

_property_ `transforms`: None

[Read-Only] The current transform of the given item - or identity in case it wasn’t found.

**Type:**

( Array\ [Transform])

### Table of Contents

- `unreal.RigUnit_GetTransformArray`
  - `RigUnit_GetTransformArray`
    - `RigUnit_GetTransformArray.initial`
    - `RigUnit_GetTransformArray.items`
    - `RigUnit_GetTransformArray.space`
    - `RigUnit_GetTransformArray.transforms`