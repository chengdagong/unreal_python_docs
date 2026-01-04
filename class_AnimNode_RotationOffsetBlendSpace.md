# unreal.AnimNode_RotationOffsetBlendSpace

```python
class unreal.AnimNode_RotationOffsetBlendSpace(blend_weight:float=0.0, internal_time_accumulator:float=0.0, base_pose:PoseLink=\[\], lod_threshold:int=0, alpha:float=0.0, alpha_scale_bias:InputScaleBias=Ellipsis, alpha_bool_blend:InputAlphaBoolBlend=Ellipsis, alpha_curve_name:Name='None', alpha_scale_bias_clamp:InputScaleBiasClamp=Ellipsis, alpha_input_type:AnimAlphaInputType=Ellipsis, alpha_bool_enabled:bool=False)
```


**Bases:** ``AnimNode_BlendSpacePlayer``


TODO:: Comment

**C++ Source:**

- **Module**: AnimGraphRuntime

- **File**: AnimNode\_RotationOffsetBlendSpace.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `alpha` (float): [Read-Write] Current strength of the AimOffset

- `alpha_bool_blend` (InputAlphaBoolBlend): [Read-Write]

- `alpha_bool_enabled` (bool): [Read-Write]

- `alpha_curve_name` (Name): [Read-Write]

- `alpha_input_type` (AnimAlphaInputType): [Read-Write]

- `alpha_scale_bias` (InputScaleBias): [Read-Write]

- `alpha_scale_bias_clamp` (InputScaleBiasClamp): [Read-Write]

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

- `loop` (bool): [Read-Write] Should the animation loop back to the start when it reaches the end?

- `method` (AnimSyncMethod): [Read-Write] How this node will synchronize with other animations. Note that this determines how the output
of this node is used for synchronization, not of animations contained by it.

- `override_position_when_joining_sync_group_as_leader` (bool): [Read-Write] When enabled, acting as the leader, and using marker-based sync, this asset player will not sync to the previous leader’s sync position when joining a sync group and before becoming the leader but instead force everyone else to match its position.

- `play_rate` (float): [Read-Write] The play rate multiplier. Can be negative, which will cause the animation to play in reverse.

- `reset_play_time_when_blend_space_changes` (bool): [Read-Write] Whether we should reset the current play time when the blend space changes

- `start_position` (float): [Read-Write] The start position in [0, 1] to use when initializing. When looping, play will still jump back to the beginning when reaching the end.

- `x` (float): [Read-Write] The X coordinate to sample in the blendspace

- `y` (float): [Read-Write] The Y coordinate to sample in the blendspace



---

_property_ `alpha`: float

[Read-Write] Current strength of the AimOffset

**Type:**

( float)


---

_property_ `alpha_bool_blend`: InputAlphaBoolBlend

[Read-Write]

**Type:**

( InputAlphaBoolBlend)


---

_property_ `alpha_bool_enabled`: bool

[Read-Write]

**Type:**

( bool)


---

_property_ `alpha_curve_name`: Name

[Read-Write]

**Type:**

( Name)


---

_property_ `alpha_input_type`: AnimAlphaInputType

[Read-Write]

**Type:**

( AnimAlphaInputType)


---

_property_ `alpha_scale_bias`: InputScaleBias

[Read-Write]

**Type:**

( InputScaleBias)


---

_property_ `alpha_scale_bias_clamp`: InputScaleBiasClamp

[Read-Write]

**Type:**

( InputScaleBiasClamp)


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

### Table of Contents

- `unreal.AnimNode_RotationOffsetBlendSpace`
  - `AnimNode_RotationOffsetBlendSpace`
    - `AnimNode_RotationOffsetBlendSpace.alpha`
    - `AnimNode_RotationOffsetBlendSpace.alpha_bool_blend`
    - `AnimNode_RotationOffsetBlendSpace.alpha_bool_enabled`
    - `AnimNode_RotationOffsetBlendSpace.alpha_curve_name`
    - `AnimNode_RotationOffsetBlendSpace.alpha_input_type`
    - `AnimNode_RotationOffsetBlendSpace.alpha_scale_bias`
    - `AnimNode_RotationOffsetBlendSpace.alpha_scale_bias_clamp`
    - `AnimNode_RotationOffsetBlendSpace.base_pose`
    - `AnimNode_RotationOffsetBlendSpace.lod_threshold`