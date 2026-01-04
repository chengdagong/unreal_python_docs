# unreal.AnimNode_BlendListByBool

```python
class unreal.AnimNode_BlendListByBool
```


**Bases:** ``AnimNode_BlendListBase``


This node is effectively a ‘branch’, picking one of two input poses based on an input Boolean value

**C++ Source:**

- **Module**: AnimGraphRuntime

- **File**: AnimNode\_BlendListByBool.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `active_value` (bool): [Read-Write] Which input should be connected to the output?

- `blend_pose` (Array[PoseLink]): [Read-Write]

- `blend_profile` (BlendProfile): [Read-Write]

- `blend_profile_for_false` (BlendProfile): [Read-Write] Used in conjunction with bUseSeperateBlendProfileForFalse

- `blend_time` (Array[float]): [Read-Write]

- `blend_type` (AlphaBlendOption): [Read-Write]

- `child_upate_mode` (BlendListChildUpdateMode): [Read-Write]

- `custom_blend_curve` (CurveFloat): [Read-Write]

- `reset_child_on_activation` (bool): [Read-Write]
deprecated: Use the ChildUpateMode instead

- `transition_type` (BlendListTransitionType): [Read-Write]

- `use_seperate_blend_profile_for_false` (bool): [Read-Write] Specify whether to use a different blend profile for the ‘false’ branch than the true branch.

- If bUseSeperateBlendProfileForFalse is false (default), then the ‘BlendProfile’ is used when ActiveValue is both true or false

- If bUseSeperateBlendProfileForFalse is true, then the ‘BlendProfileForFalse’ value is used when the ActiveValue is false, but ‘BlendProfile’ is used when ActiveValue is true


### Table of Contents

- `unreal.AnimNode_BlendListByBool`
  - `AnimNode_BlendListByBool`