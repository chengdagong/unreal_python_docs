# unreal.RigUnit_GetInitialBoneTransform

```python
class unreal.RigUnit_GetInitialBoneTransform(bone:Name='None', space:RigVMTransformSpace=Ellipsis, transform:Transform=Ellipsis)
```


**Bases:** ``RigUnit``


GetInitialBoneTransform is used to retrieve a single transform from a hierarchy.

**C++ Source:**

- **Plugin**: ControlRig

- **Module**: ControlRig

- **File**: RigUnit\_GetInitialBoneTransform.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `bone` (Name): [Read-Write] The name of the Bone to retrieve the transform for.

- `space` (RigVMTransformSpace): [Read-Write] Defines if the bone’s transform should be retrieved
in local or global space.

- `transform` (Transform): [Read-Write] The current transform of the given bone - or identity in case it wasn’t found.



---

_property_ `bone`: Name

[Read-Write] The name of the Bone to retrieve the transform for.

**Type:**

( Name)


---

_property_ `space`: RigVMTransformSpace

[Read-Write] Defines if the bone’s transform should be retrieved
in local or global space.

**Type:**

( RigVMTransformSpace)


---

_property_ `transform`: Transform

[Read-Only] The current transform of the given bone - or identity in case it wasn’t found.

**Type:**

( Transform)

### Table of Contents

- `unreal.RigUnit_GetInitialBoneTransform`
  - `RigUnit_GetInitialBoneTransform`
    - `RigUnit_GetInitialBoneTransform.bone`
    - `RigUnit_GetInitialBoneTransform.space`
    - `RigUnit_GetInitialBoneTransform.transform`