# unreal.RigUnit_ModifyBoneTransforms

```python
class unreal.RigUnit_ModifyBoneTransforms(execute_pin:RigVMExecutePin=\[\], bone_to_modify:None=\[\], weight:float=0.0, weight_minimum:float=0.0, weight_maximum:float=0.0, mode:ControlRigModifyBoneMode=Ellipsis)
```


**Bases:** ``RigUnit_HighlevelBaseMutable``


ModifyBonetransforms is used to perform a change in the hierarchy by setting one or more bones’ transforms.

**C++ Source:**

- **Plugin**: ControlRig

- **Module**: ControlRig

- **File**: RigUnit\_ModifyBoneTransforms.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `bone_to_modify` (Array[RigUnit\_ModifyBoneTransforms\_PerBone]): [Read-Write] The bones to modify.

- `execute_pin` (RigVMExecutePin): [Read-Write] \* This property is used to chain multiple mutable units together

- `mode` (ControlRigModifyBoneMode): [Read-Only] Defines if the bone’s transform should be set
in local or global space, additive or override.

- `weight` (float): [Read-Write] At 1 this sets the transform, between 0 and 1 the transform is blended with previous results.

- `weight_maximum` (float): [Read-Only] The maximum of the weight - defaults to 1.0

- `weight_minimum` (float): [Read-Only] The minimum of the weight - defaults to 0.0



---

_property_ `bone_to_modify`: None

[Read-Write] The bones to modify.

**Type:**

( Array\ [RigUnit\_ModifyBoneTransforms\_PerBone])


---

_property_ `mode`: ControlRigModifyBoneMode

[Read-Only] Defines if the bone’s transform should be set
in local or global space, additive or override.

**Type:**

( ControlRigModifyBoneMode)


---

_property_ `weight`: float

[Read-Write] At 1 this sets the transform, between 0 and 1 the transform is blended with previous results.

**Type:**

( float)


---

_property_ `weight_maximum`: float

[Read-Only] The maximum of the weight - defaults to 1.0

**Type:**

( float)


---

_property_ `weight_minimum`: float

[Read-Only] The minimum of the weight - defaults to 0.0

**Type:**

( float)

### Table of Contents

- `unreal.RigUnit_ModifyBoneTransforms`
  - `RigUnit_ModifyBoneTransforms`
    - `RigUnit_ModifyBoneTransforms.bone_to_modify`
    - `RigUnit_ModifyBoneTransforms.mode`
    - `RigUnit_ModifyBoneTransforms.weight`
    - `RigUnit_ModifyBoneTransforms.weight_maximum`
    - `RigUnit_ModifyBoneTransforms.weight_minimum`