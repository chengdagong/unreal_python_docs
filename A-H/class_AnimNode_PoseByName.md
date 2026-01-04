# unreal.AnimNode_PoseByName

```python
class unreal.AnimNode_PoseByName(blend_weight:float=0.0, internal_time_accumulator:float=0.0, pose_asset:PoseAsset=Ellipsis, pose_name:Name='None', pose_weight:float=0.0)
```


**Bases:** ``AnimNode_PoseHandler``


Evaluates a point in an anim sequence, using a specific time input rather than advancing time internally.
Typically the playback position of the animation for this node will represent something other than time, like jump height.
This node will not trigger any notifies present in the associated sequence.

**C++ Source:**

- **Module**: AnimGraphRuntime

- **File**: AnimNode\_PoseByName.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `blend_weight` (float): [Read-Write] Last encountered blendweight for this node

- `internal_time_accumulator` (float): [Read-Write] Accumulated time used to reference the asset in this node

- `pose_asset` (PoseAsset): [Read-Write] The animation sequence asset to evaluate

- `pose_name` (Name): [Read-Write]

- `pose_weight` (float): [Read-Write]



---

_property_ `pose_name`: Name

[Read-Write]

**Type:**

( Name)


---

_property_ `pose_weight`: float

[Read-Write]

**Type:**

( float)

### Table of Contents

- `unreal.AnimNode_PoseByName`
  - `AnimNode_PoseByName`
    - `AnimNode_PoseByName.pose_name`
    - `AnimNode_PoseByName.pose_weight`