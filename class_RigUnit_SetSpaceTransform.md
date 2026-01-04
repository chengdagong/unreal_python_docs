# unreal.RigUnit_SetSpaceTransform

```python
class unreal.RigUnit_SetSpaceTransform(execute_pin:RigVMExecutePin=\[\], space:Name='None', weight:float=0.0, transform:Transform=Ellipsis, space_type:RigVMTransformSpace=Ellipsis)
```


**Bases:** ``RigUnitMutable``


SetSpaceTransform is used to perform a change in the hierarchy by setting a single space’s transform.

**C++ Source:**

- **Plugin**: ControlRig

- **Module**: ControlRig

- **File**: RigUnit\_SetSpaceTransform.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `execute_pin` (RigVMExecutePin): [Read-Write] \* This property is used to chain multiple mutable units together

- `space` (Name): [Read-Write] The name of the Space to set the transform for.

- `space_type` (RigVMTransformSpace): [Read-Write] Defines if the bone’s transform should be set
in local or global space.

- `transform` (Transform): [Read-Write] The transform value to set for the given Space.

- `weight` (float): [Read-Write] The weight of the change - how much the change should be applied



---

_property_ `space`: Name

[Read-Write] The name of the Space to set the transform for.

**Type:**

( Name)


---

_property_ `space_type`: RigVMTransformSpace

[Read-Write] Defines if the bone’s transform should be set
in local or global space.

**Type:**

( RigVMTransformSpace)


---

_property_ `transform`: Transform

[Read-Write] The transform value to set for the given Space.

**Type:**

( Transform)


---

_property_ `weight`: float

[Read-Write] The weight of the change - how much the change should be applied

**Type:**

( float)

### Table of Contents

- `unreal.RigUnit_SetSpaceTransform`
  - `RigUnit_SetSpaceTransform`
    - `RigUnit_SetSpaceTransform.space`
    - `RigUnit_SetSpaceTransform.space_type`
    - `RigUnit_SetSpaceTransform.transform`
    - `RigUnit_SetSpaceTransform.weight`