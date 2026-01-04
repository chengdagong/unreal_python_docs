# unreal.AnimNode_BlendListByInt

```python
class unreal.AnimNode_BlendListByInt
```


**Bases:** ``AnimNode_BlendListBase``


Blend list node; has many children

**C++ Source:**

- **Module**: AnimGraphRuntime

- **File**: AnimNode\_BlendListByInt.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `active_child_index` (int32): [Read-Write]

- `blend_pose` (Array[PoseLink]): [Read-Write]

- `blend_profile` (BlendProfile): [Read-Write]

- `blend_time` (Array[float]): [Read-Write]

- `blend_type` (AlphaBlendOption): [Read-Write]

- `child_upate_mode` (BlendListChildUpdateMode): [Read-Write]

- `custom_blend_curve` (CurveFloat): [Read-Write]

- `reset_child_on_activation` (bool): [Read-Write]
deprecated: Use the ChildUpateMode instead

- `transition_type` (BlendListTransitionType): [Read-Write]


### Table of Contents

- `unreal.AnimNode_BlendListByInt`
  - `AnimNode_BlendListByInt`