# unreal.AnimNode_AimOffsetLookAt

```python
class unreal.AnimNode_AimOffsetLookAt(blend_weight:float=0.0, internal_time_accumulator:float=0.0, base_pose:PoseLink=\[\], lod_threshold:int=0, source_socket_name:Name='None', pivot_socket_name:Name='None', look_at_location:Vector=Ellipsis, socket_axis:Vector=Ellipsis, alpha:float=0.0)
```


**Bases:** ``AnimNode_BlendSpacePlayer``


This node uses a source transform of a socket on the skeletal mesh to automatically calculate
Yaw and Pitch directions for a referenced aim offset given a point in the world to look at.

**C++ Source:**

- **Module**: AnimGraphRuntime

- **File**: AnimNode\_AimOffsetLookAt.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `alpha` (float): [Read-Write] Amount of this node to blend into the output pose

- `base_pose` (PoseLink): [Read-Write]

- `blend_space` (BlendSpace): [Read-Write] The blendspace asset to play

- `blend_weight` (float): [Read-Write] Last encountered blendweight for this node

- `group_name` (Name): [Read-Write] The group name that we synchronize with (NAME\_None if it is not part of any group). Note that
this is the name of the group used to sync the output of this node - it will not force
syncing of animations contained by it.

- `group_role` (AnimGroupRole): [Read-Write] The role this node can assume within the group (ignored if GroupName is not set). Note
that this is the role of the output of this node, not of animations contained by it.

- `ignore_for_relevancy_test` (bool): [Read-Write] If true, “Relevant anim” nodes that look for the highest weighted animation in a state will ignore this node

- `internal_time_accumulator` (float): [Read-Write] Accumulated time used to reference the asset in this node

- `lod_threshold` (int32): [Read-Write] \* Max LOD that this node is allowed to run
\\* For example if you have LODThreshold to be 2, it will run until LOD 2 (based on 0 index)
\\* when the component LOD becomes 3, it will stop update/evaluate
\\* currently transition would be issue and that has to be re-visited

- `look_at_location` (Vector): [Read-Write] Location, in world space to look at

- `loop` (bool): [Read-Write] Should the animation loop back to the start when it reaches the end?

- `method` (AnimSyncMethod): [Read-Write] How this node will synchronize with other animations. Note that this determines how the output
of this node is used for synchronization, not of animations contained by it.

- `override_position_when_joining_sync_group_as_leader` (bool): [Read-Write] When enabled, acting as the leader, and using marker-based sync, this asset player will not sync to the previous leader’s sync position when joining a sync group and before becoming the leader but instead force everyone else to match its position.

- `pivot_socket_name` (Name): [Read-Write] Socket or bone to treat as the look at pivot (optional). This will overwrite the translation of the
source socket transform improve the lookat direction, especially when the target is close
to the character

- `play_rate` (float): [Read-Write] The play rate multiplier. Can be negative, which will cause the animation to play in reverse.

- `reset_play_time_when_blend_space_changes` (bool): [Read-Write] Whether we should reset the current play time when the blend space changes

- `socket_axis` (Vector): [Read-Write] Direction in the socket transform to consider the ‘forward’ or look at axis

- `source_socket_name` (Name): [Read-Write] Socket or bone to treat as the look at source. This will then be pointed at LookAtLocation

- `start_position` (float): [Read-Write] The start position in [0, 1] to use when initializing. When looping, play will still jump back to the beginning when reaching the end.

- `x` (float): [Read-Write] The X coordinate to sample in the blendspace

- `y` (float): [Read-Write] The Y coordinate to sample in the blendspace



---

_property_ `alpha`: float

[Read-Write] Amount of this node to blend into the output pose

**Type:**

( float)


---

_property_ `base_pose`: PoseLink

[Read-Write]

**Type:**

( PoseLink)


---

_property_ `lod_threshold`: int

[Read-Write] \* Max LOD that this node is allowed to run
\\* For example if you have LODThreshold to be 2, it will run until LOD 2 (based on 0 index)
\\* when the component LOD becomes 3, it will stop update/evaluate
\\* currently transition would be issue and that has to be re-visited

**Type:**

(int32)


---

_property_ `look_at_location`: Vector

[Read-Write] Location, in world space to look at

**Type:**

( Vector)


---

_property_ `pivot_socket_name`: Name

[Read-Write] Socket or bone to treat as the look at pivot (optional). This will overwrite the translation of the
source socket transform improve the lookat direction, especially when the target is close
to the character

**Type:**

( Name)


---

_property_ `socket_axis`: Vector

[Read-Write] Direction in the socket transform to consider the ‘forward’ or look at axis

**Type:**

( Vector)


---

_property_ `source_socket_name`: Name

[Read-Write] Socket or bone to treat as the look at source. This will then be pointed at LookAtLocation

**Type:**

( Name)

### Table of Contents

- `unreal.AnimNode_AimOffsetLookAt`
  - `AnimNode_AimOffsetLookAt`
    - `AnimNode_AimOffsetLookAt.alpha`
    - `AnimNode_AimOffsetLookAt.base_pose`
    - `AnimNode_AimOffsetLookAt.lod_threshold`
    - `AnimNode_AimOffsetLookAt.look_at_location`
    - `AnimNode_AimOffsetLookAt.pivot_socket_name`
    - `AnimNode_AimOffsetLookAt.socket_axis`
    - `AnimNode_AimOffsetLookAt.source_socket_name`