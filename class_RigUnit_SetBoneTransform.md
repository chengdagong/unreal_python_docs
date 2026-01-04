# unreal.RigUnit_SetBoneTransform

```python
class unreal.RigUnit_SetBoneTransform(execute_pin:RigVMExecutePin=\[\], bone:Name='None', transform:Transform=Ellipsis, result:Transform=Ellipsis, space:RigVMTransformSpace=Ellipsis, weight:float=0.0, propagate_to_children:bool=False)
```


**Bases:** ``RigUnitMutable``


SetBoneTransform is used to perform a change in the hierarchy by setting a single bone’s transform.

**C++ Source:**

- **Plugin**: ControlRig

- **Module**: ControlRig

- **File**: RigUnit\_SetBoneTransform.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `bone` (Name): [Read-Write] The name of the Bone to set the transform for.

- `execute_pin` (RigVMExecutePin): [Read-Write] \* This property is used to chain multiple mutable units together

- `propagate_to_children` (bool): [Read-Only] If set to true all of the global transforms of the children
of this bone will be recalculated based on their local transforms.
Note: This is computationally more expensive than turning it off.

- `result` (Transform): [Read-Write] The transform value result (after weighting)

- `space` (RigVMTransformSpace): [Read-Write] Defines if the bone’s transform should be set
in local or global space.

- `transform` (Transform): [Read-Write] The transform value to set for the given Bone.

- `weight` (float): [Read-Write] The weight of the change - how much the change should be applied



---

_property_ `bone`: Name

[Read-Write] The name of the Bone to set the transform for.

**Type:**

( Name)


---

_property_ `propagate_to_children`: bool

[Read-Only] If set to true all of the global transforms of the children
of this bone will be recalculated based on their local transforms.
Note: This is computationally more expensive than turning it off.

**Type:**

( bool)


---

_property_ `result`: Transform

[Read-Only] The transform value result (after weighting)

**Type:**

( Transform)


---

_property_ `space`: RigVMTransformSpace

[Read-Write] Defines if the bone’s transform should be set
in local or global space.

**Type:**

( RigVMTransformSpace)


---

_property_ `transform`: Transform

[Read-Write] The transform value to set for the given Bone.

**Type:**

( Transform)


---

_property_ `weight`: float

[Read-Write] The weight of the change - how much the change should be applied

**Type:**

( float)

### Table of Contents

- `unreal.RigUnit_SetBoneTransform`
  - `RigUnit_SetBoneTransform`
    - `RigUnit_SetBoneTransform.bone`
    - `RigUnit_SetBoneTransform.propagate_to_children`
    - `RigUnit_SetBoneTransform.result`
    - `RigUnit_SetBoneTransform.space`
    - `RigUnit_SetBoneTransform.transform`
    - `RigUnit_SetBoneTransform.weight`