# unreal.AnimNode_BlendListByEnum

```python
class unreal.AnimNode_BlendListByEnum
```


**Bases:** ``AnimNode_BlendListBase``


Blend List by Enum, it changes based on enum input that enters

**C++ Source:**

- **Module**: AnimGraphRuntime

- **File**: AnimNode\_BlendListByEnum.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `active_enum_value` (uint8): [Read-Write] The currently selected pose (as an enum value)

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

- `unreal.AnimNode_BlendListByEnum`
  - `AnimNode_BlendListByEnum`