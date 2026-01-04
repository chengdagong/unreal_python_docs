# unreal.AnimNode_PoseHandler

```python
class unreal.AnimNode_PoseHandler(blend_weight:float=0.0, internal_time_accumulator:float=0.0, pose_asset:PoseAsset=Ellipsis)
```


**Bases:** ``AnimNode_AssetPlayerBase``


Evaluates a point in an anim sequence, using a specific time input rather than advancing time internally.
Typically the playback position of the animation for this node will represent something other than time, like jump height.
This node will not trigger any notifies present in the associated sequence.

**C++ Source:**

- **Module**: AnimGraphRuntime

- **File**: AnimNode\_PoseHandler.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `blend_weight` (float): [Read-Write] Last encountered blendweight for this node

- `internal_time_accumulator` (float): [Read-Write] Accumulated time used to reference the asset in this node

- `pose_asset` (PoseAsset): [Read-Write] The animation sequence asset to evaluate



---

_property_ `pose_asset`: PoseAsset

[Read-Write] The animation sequence asset to evaluate

**Type:**

( PoseAsset)

### Table of Contents

- `unreal.AnimNode_PoseHandler`
  - `AnimNode_PoseHandler`
    - `AnimNode_PoseHandler.pose_asset`