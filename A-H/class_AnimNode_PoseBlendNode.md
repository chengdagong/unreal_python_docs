# unreal.AnimNode_PoseBlendNode

```python
class unreal.AnimNode_PoseBlendNode(blend_weight:float=0.0, internal_time_accumulator:float=0.0, pose_asset:PoseAsset=Ellipsis, source_pose:PoseLink=\[\])
```


**Bases:** ``AnimNode_PoseHandler``


Evaluates a point in an anim sequence, using a specific time input rather than advancing time internally.
Typically the playback position of the animation for this node will represent something other than time, like jump height.
This node will not trigger any notifies present in the associated sequence.

**C++ Source:**

- **Module**: AnimGraphRuntime

- **File**: AnimNode\_PoseBlendNode.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `blend_option` (AlphaBlendOption): [Read-Write] Type of blending used (Linear, Cubic, etc.)

- `blend_weight` (float): [Read-Write] Last encountered blendweight for this node

- `custom_curve` (CurveFloat): [Read-Write] If you’re using Custom BlendOption, you can specify curve

- `internal_time_accumulator` (float): [Read-Write] Accumulated time used to reference the asset in this node

- `pose_asset` (PoseAsset): [Read-Write] The animation sequence asset to evaluate

- `source_pose` (PoseLink): [Read-Write]



---

_property_ `source_pose`: PoseLink

[Read-Write]

**Type:**

( PoseLink)

### Table of Contents

- `unreal.AnimNode_PoseBlendNode`
  - `AnimNode_PoseBlendNode`
    - `AnimNode_PoseBlendNode.source_pose`