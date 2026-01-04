# unreal.RigUnit_GetRelativeBoneTransform

```python
class unreal.RigUnit_GetRelativeBoneTransform(bone:Name='None', space:Name='None', transform:Transform=Ellipsis)
```


**Bases:** ``RigUnit``


GetBoneTransform is used to retrieve a single transform from a hierarchy.

**C++ Source:**

- **Plugin**: ControlRig

- **Module**: ControlRig

- **File**: RigUnit\_GetRelativeBoneTransform.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `bone` (Name): [Read-Write] The name of the Bone to retrieve the transform for.

- `space` (Name): [Read-Write] The name of the Bone to retrieve the transform relative within.

- `transform` (Transform): [Read-Write] The current transform of the given bone - or identity in case it wasn’t found.



---

_property_ `bone`: Name

[Read-Write] The name of the Bone to retrieve the transform for.

**Type:**

( Name)


---

_property_ `space`: Name

[Read-Write] The name of the Bone to retrieve the transform relative within.

**Type:**

( Name)


---

_property_ `transform`: Transform

[Read-Only] The current transform of the given bone - or identity in case it wasn’t found.

**Type:**

( Transform)

### Table of Contents

- `unreal.RigUnit_GetRelativeBoneTransform`
  - `RigUnit_GetRelativeBoneTransform`
    - `RigUnit_GetRelativeBoneTransform.bone`
    - `RigUnit_GetRelativeBoneTransform.space`
    - `RigUnit_GetRelativeBoneTransform.transform`