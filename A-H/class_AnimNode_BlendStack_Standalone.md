# unreal.AnimNode_BlendStack_Standalone

```python
class unreal.AnimNode_BlendStack_Standalone(blend_weight:float=0.0, internal_time_accumulator:float=0.0, stitch_database:Object=Ellipsis, stitch_blend_time:float=0.0, stitch_blend_max_cost:float=0.0, notify_recency_time_out:float=0.0)
```


**Bases:** ``AnimNode_AssetPlayerBase``


namespace UE::BlendStack

**C++ Source:**

- **Plugin**: BlendStack

- **Module**: BlendStack

- **File**: AnimNode\_BlendStack.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `blend_weight` (float): [Read-Write] Last encountered blendweight for this node

- `internal_time_accumulator` (float): [Read-Write] Accumulated time used to reference the asset in this node

- `max_active_blends` (int32): [Read-Write] Number of max active blending animation in the blend stack. If MaxActiveBlends is zero then blend stack is disabled

- `max_blend_in_time_to_override_animation` (float): [Read-Write] if the most relevant (recently added) animation is within MaxBlendInTimeToOverrideAnimation, the new requested blend will take its spot
otherwise a new blended will be added to the stack

- `notify_recency_time_out` (float): [Read-Write] Window of time after firing a notify that any instance of the same notify will be filtered out.

- `player_depth_blend_in_time_multiplier` (float): [Read-Write] AnimPlayers blend in timer will be incremented PlayerDepthBlendInTimeMultiplier times faster on a deeper blend

- `should_filter_notifies` (bool): [Read-Write] Flag that determines if any notifies from originating from an anim player samples should be filtered or not.

- `stitch_blend_max_cost` (float): [Read-Write] if the cost from searching StitchDatabase is above StitchBlendMaxCost, blend stack will perform a regular blend,
and not using the returned stitch animation as blend

- `stitch_blend_time` (float): [Read-Write] blend time in seconds used to blend into and out from a stitch animation

- `stitch_database` (Object): [Read-Write] database used to search for an animation stitch to use as blend

- `store_blended_pose` (bool): [Read-Write] if the number of requested blends is higher than MaxActiveBlends, blend stack will blend and accumulate
into a stored pose all the overflowing animations. if bStoreBlendedPose is false, the memory to store the pose will be saved,
but once reached the MaxActiveBlends, blendstack will start discarding animations, potentially resulting in animation pops



---

_property_ `notify_recency_time_out`: float

[Read-Write] Window of time after firing a notify that any instance of the same notify will be filtered out.

**Type:**

( float)


---

_property_ `stitch_blend_max_cost`: float

[Read-Write] if the cost from searching StitchDatabase is above StitchBlendMaxCost, blend stack will perform a regular blend,
and not using the returned stitch animation as blend

**Type:**

( float)


---

_property_ `stitch_blend_time`: float

[Read-Write] blend time in seconds used to blend into and out from a stitch animation

**Type:**

( float)


---

_property_ `stitch_database`: Object

[Read-Write] database used to search for an animation stitch to use as blend

**Type:**

( Object)

### Table of Contents

- `unreal.AnimNode_BlendStack_Standalone`
  - `AnimNode_BlendStack_Standalone`
    - `AnimNode_BlendStack_Standalone.notify_recency_time_out`
    - `AnimNode_BlendStack_Standalone.stitch_blend_max_cost`
    - `AnimNode_BlendStack_Standalone.stitch_blend_time`
    - `AnimNode_BlendStack_Standalone.stitch_database`