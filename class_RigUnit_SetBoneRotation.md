# unreal.RigUnit_SetBoneRotation

```python
class unreal.RigUnit_SetBoneRotation(execute_pin:RigVMExecutePin=\[\], bone:Name='None', rotation:Quat=Ellipsis, space:RigVMTransformSpace=Ellipsis, weight:float=0.0, propagate_to_children:bool=False)
```


**Bases:** ``RigUnitMutable``


SetBoneRotation is used to perform a change in the hierarchy by setting a single bone’s rotation.

**C++ Source:**

- **Plugin**: ControlRig

- **Module**: ControlRig

- **File**: RigUnit\_SetBoneRotation.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `bone` (Name): [Read-Write] The name of the Bone to set the rotation for.

- `execute_pin` (RigVMExecutePin): [Read-Write] \* This property is used to chain multiple mutable units together

- `propagate_to_children` (bool): [Read-Only] If set to true all of the global transforms of the children
of this bone will be recalculated based on their local transforms.
Note: This is computationally more expensive than turning it off.

- `rotation` (Quat): [Read-Write] The rotation value to set for the given Bone.

- `space` (RigVMTransformSpace): [Read-Write] Defines if the bone’s rotation should be set
in local or global space.

- `weight` (float): [Read-Write] The weight of the change - how much the change should be applied



---

_property_ `bone`: Name

[Read-Write] The name of the Bone to set the rotation for.

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

_property_ `rotation`: Quat

[Read-Write] The rotation value to set for the given Bone.

**Type:**

( Quat)


---

_property_ `space`: RigVMTransformSpace

[Read-Write] Defines if the bone’s rotation should be set
in local or global space.

**Type:**

( RigVMTransformSpace)


---

_property_ `weight`: float

[Read-Write] The weight of the change - how much the change should be applied

**Type:**

( float)

### Table of Contents

- `unreal.RigUnit_SetBoneRotation`
  - `RigUnit_SetBoneRotation`
    - `RigUnit_SetBoneRotation.bone`
    - `RigUnit_SetBoneRotation.propagate_to_children`
    - `RigUnit_SetBoneRotation.rotation`
    - `RigUnit_SetBoneRotation.space`
    - `RigUnit_SetBoneRotation.weight`