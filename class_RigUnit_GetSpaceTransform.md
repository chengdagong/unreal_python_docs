# unreal.RigUnit_GetSpaceTransform

```python
class unreal.RigUnit_GetSpaceTransform(space:Name='None', space_type:RigVMTransformSpace=Ellipsis, transform:Transform=Ellipsis)
```


**Bases:** ``RigUnit``


GetSpaceTransform is used to retrieve a single transform from a hierarchy.

**C++ Source:**

- **Plugin**: ControlRig

- **Module**: ControlRig

- **File**: RigUnit\_GetSpaceTransform.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `space` (Name): [Read-Write] The name of the Space to retrieve the transform for.

- `space_type` (RigVMTransformSpace): [Read-Write] Defines if the Space’s transform should be retrieved
in local or global space.

- `transform` (Transform): [Read-Write] The current transform of the given bone - or identity in case it wasn’t found.



---

_property_ `space`: Name

[Read-Write] The name of the Space to retrieve the transform for.

**Type:**

( Name)


---

_property_ `space_type`: RigVMTransformSpace

[Read-Write] Defines if the Space’s transform should be retrieved
in local or global space.

**Type:**

( RigVMTransformSpace)


---

_property_ `transform`: Transform

[Read-Only] The current transform of the given bone - or identity in case it wasn’t found.

**Type:**

( Transform)

### Table of Contents

- `unreal.RigUnit_GetSpaceTransform`
  - `RigUnit_GetSpaceTransform`
    - `RigUnit_GetSpaceTransform.space`
    - `RigUnit_GetSpaceTransform.space_type`
    - `RigUnit_GetSpaceTransform.transform`