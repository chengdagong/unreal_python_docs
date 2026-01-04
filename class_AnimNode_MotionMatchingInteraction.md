# unreal.AnimNode_MotionMatchingInteraction

```python
class unreal.AnimNode_MotionMatchingInteraction(blend_weight:float=0.0, internal_time_accumulator:float=0.0, stitch_database:Object=Ellipsis, stitch_blend_time:float=0.0, stitch_blend_max_cost:float=0.0, notify_recency_time_out:float=0.0, blend_time:float=0.0, blend_profile:BlendProfile=Ellipsis, blend_option:AlphaBlendOption=Ellipsis)
```


**Bases:** ``AnimNode_BlendStack_Standalone``


Anim Node Motion Matching Interaction

**C++ Source:**

- **Plugin**: PoseSearch

- **Module**: PoseSearch

- **File**: AnimNode\_MotionMatchingInteraction.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `availabilities` (Array[PoseSearchInteractionAvailability]): [Read-Write]

- `blend_option` (AlphaBlendOption): [Read-Write]

- `blend_profile` (BlendProfile): [Read-Write]

- `blend_time` (float): [Read-Write] tunable animation transition blend time

- `blend_weight` (float): [Read-Write] Last encountered blendweight for this node

- `blendspace_update_mode` (BlendStack\_BlendspaceUpdateMode): [Read-Write] How we should update individual blend space parameters. See dropdown options tooltips.

- `internal_time_accumulator` (float): [Read-Write] Accumulated time used to reference the asset in this node

- `max_active_blends` (int32): [Read-Write] Number of max active blending animation in the blend stack. If MaxActiveBlends is zero then blend stack is disabled

- `max_blend_in_time_to_override_animation` (float): [Read-Write] if the most relevant (recently added) animation is within MaxBlendInTimeToOverrideAnimation, the new requested blend will take its spot
otherwise a new blended will be added to the stack

- `notify_recency_time_out` (float): [Read-Write] Window of time after firing a notify that any instance of the same notify will be filtered out.

- `player_depth_blend_in_time_multiplier` (float): [Read-Write] AnimPlayers blend in timer will be incremented PlayerDepthBlendInTimeMultiplier times faster on a deeper blend

- `reset_on_becoming_relevant` (bool): [Read-Write] Reset the blend stack if it has become relevant to the graph after not being updated on previous frames.

- `should_filter_notifies` (bool): [Read-Write] Flag that determines if any notifies from originating from an anim player samples should be filtered or not.

- `stitch_blend_max_cost` (float): [Read-Write] if the cost from searching StitchDatabase is above StitchBlendMaxCost, blend stack will perform a regular blend,
and not using the returned stitch animation as blend

- `stitch_blend_time` (float): [Read-Write] blend time in seconds used to blend into and out from a stitch animation

- `stitch_database` (Object): [Read-Write] database used to search for an animation stitch to use as blend

- `store_blended_pose` (bool): [Read-Write] if the number of requested blends is higher than MaxActiveBlends, blend stack will blend and accumulate
into a stored pose all the overflowing animations. if bStoreBlendedPose is false, the memory to store the pose will be saved,
but once reached the MaxActiveBlends, blendstack will start discarding animations, potentially resulting in animation pops

- `use_inertial_blend` (bool): [Read-Write] tunable animation transition blend time

- `validate_result_against_availabilities` (bool): [Read-Write]

- `warp_using_root_bone` (bool): [Read-Write] if bWarpUsingRootBone is true, warping will be calculated using the interacting actors previous frame root bone transforms (effective for setups with OffsetRootBone node allowing root bone drifting from capsule)
if bWarpUsingRootBone is true, warping will be calculated using the previous frame root transforms (effective root motion driven for setups)

- `warping_rotation_ratio` (float): [Read-Write] amount or rotation warping to apply

- `warping_translation_ratio` (float): [Read-Write] amount or translation warping to apply



---

_property_ `blend_option`: AlphaBlendOption

[Read-Write]

**Type:**

( AlphaBlendOption)


---

_property_ `blend_profile`: BlendProfile

[Read-Write]

**Type:**

( BlendProfile)


---

_property_ `blend_time`: float

[Read-Write] tunable animation transition blend time

**Type:**

( float)

### Table of Contents

- `unreal.AnimNode_MotionMatchingInteraction`
  - `AnimNode_MotionMatchingInteraction`
    - `AnimNode_MotionMatchingInteraction.blend_option`
    - `AnimNode_MotionMatchingInteraction.blend_profile`
    - `AnimNode_MotionMatchingInteraction.blend_time`