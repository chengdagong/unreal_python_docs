# unreal.AnimNode_BlendListBase

```python
class unreal.AnimNode_BlendListBase
```


**Bases:** ``AnimNode_Base``


Blend list node; has many children

**C++ Source:**

- **Module**: AnimGraphRuntime

- **File**: AnimNode\_BlendListBase.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `blend_pose` (Array[PoseLink]): [Read-Write]

- `blend_profile` (BlendProfile): [Read-Write]

- `blend_time` (Array[float]): [Read-Write]

- `blend_type` (AlphaBlendOption): [Read-Write]

- `child_upate_mode` (BlendListChildUpdateMode): [Read-Write]

- `custom_blend_curve` (CurveFloat): [Read-Write]

- `reset_child_on_activation` (bool): [Read-Write]
deprecated: Use the ChildUpateMode instead

- `transition_type` (BlendListTransitionType): [Read-Write]



---

_property_ `reset_child_on_activation`: bool

[Read-Write]
deprecated: Use the ChildUpateMode instead

**Type:**

( bool)

### Table of Contents

- `unreal.AnimNode_BlendListBase`
  - `AnimNode_BlendListBase`
    - `AnimNode_BlendListBase.reset_child_on_activation`