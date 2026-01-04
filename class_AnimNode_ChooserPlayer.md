# unreal.AnimNode_ChooserPlayer

```python
class unreal.AnimNode_ChooserPlayer(blend_weight:float=0.0, internal_time_accumulator:float=0.0, stitch_database:Object=Ellipsis, stitch_blend_time:float=0.0, stitch_blend_max_cost:float=0.0, notify_recency_time_out:float=0.0, blend_space_x:float=0.0, blend_space_y:float=0.0, default_settings:ChooserPlayerSettings=Ellipsis)
```


**Bases:** ``AnimNode_BlendStack_Standalone``


Anim Node Chooser Player

**C++ Source:**

- **Plugin**: Chooser

- **Module**: Chooser

- **File**: AnimNode\_ChooserPlayer.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `blend_space_x` (float): [Read-Write] requested blend space blend X parameter (if AnimationAsset is a blend space)

- `blend_space_y` (float): [Read-Write] requested blend space blend Y parameter (if AnimationAsset is a blend space)

- `blend_weight` (float): [Read-Write] Last encountered blendweight for this node

- `chooser` (InstancedStruct): [Read-Write] Type of chooser logic to use: Use “Evaluate Chooser” for chooser table evaluation, and “Lookup Proxy” for proxy table lookups

- `default_settings` (ChooserPlayerSettings): [Read-Write] Settings when starting an animation - these can be overridden per animation asset by the chooser itself

- `evaluation_frequency` (ChooserEvaluationFrequency): [Read-Write] How often the chooser should be evaluated

- `group_name` (Name): [Read-Write] The group name that we synchronize with (NAME\_None if it is not part of any group). Note that
this is the name of the group used to sync the output of this node - it will not force
syncing of animations contained by it.

- `group_role` (AnimGroupRole): [Read-Write] The role this node can assume within the group (ignored if GroupName is not set). Note
that this is the role of the output of this node, not of animations contained by it.

- `ignore_for_relevancy_test` (bool): [Read-Write] If true, “Relevant anim” nodes that look for the highest weighted animation in a state will ignore this node

- `internal_time_accumulator` (float): [Read-Write] Accumulated time used to reference the asset in this node

- `max_active_blends` (int32): [Read-Write] Number of max active blending animation in the blend stack. If MaxActiveBlends is zero then blend stack is disabled

- `max_blend_in_time_to_override_animation` (float): [Read-Write] if the most relevant (recently added) animation is within MaxBlendInTimeToOverrideAnimation, the new requested blend will take its spot
otherwise a new blended will be added to the stack

- `method` (AnimSyncMethod): [Read-Write] How this node will synchronize with other animations. Note that this determines how the output
of this node is used for synchronization, not of animations contained by it.

- `mirror_data_table` (MirrorDataTable): [Read-Write] if set and bMirrored MirrorDataTable will be used for mirroring the aniamtion

- `notify_recency_time_out` (float): [Read-Write] Window of time after firing a notify that any instance of the same notify will be filtered out.

- `player_depth_blend_in_time_multiplier` (float): [Read-Write] AnimPlayers blend in timer will be incremented PlayerDepthBlendInTimeMultiplier times faster on a deeper blend

- `should_filter_notifies` (bool): [Read-Write] Flag that determines if any notifies from originating from an anim player samples should be filtered or not.

- `start_from_matching_pose` (bool): [Read-Write] Use pose matching to choose the start position. Requires PoseSearch plugin.

- `stitch_blend_max_cost` (float): [Read-Write] if the cost from searching StitchDatabase is above StitchBlendMaxCost, blend stack will perform a regular blend,
and not using the returned stitch animation as blend

- `stitch_blend_time` (float): [Read-Write] blend time in seconds used to blend into and out from a stitch animation

- `stitch_database` (Object): [Read-Write] database used to search for an animation stitch to use as blend

- `store_blended_pose` (bool): [Read-Write] if the number of requested blends is higher than MaxActiveBlends, blend stack will blend and accumulate
into a stored pose all the overflowing animations. if bStoreBlendedPose is false, the memory to store the pose will be saved,
but once reached the MaxActiveBlends, blendstack will start discarding animations, potentially resulting in animation pops



---

_property_ `blend_space_x`: float

[Read-Write] requested blend space blend X parameter (if AnimationAsset is a blend space)

**Type:**

( float)


---

_property_ `blend_space_y`: float

[Read-Write] requested blend space blend Y parameter (if AnimationAsset is a blend space)

**Type:**

( float)


---

_property_ `default_settings`: ChooserPlayerSettings

[Read-Write] Settings when starting an animation - these can be overridden per animation asset by the chooser itself

**Type:**

( ChooserPlayerSettings)

### Table of Contents

- `unreal.AnimNode_ChooserPlayer`
  - `AnimNode_ChooserPlayer`
    - `AnimNode_ChooserPlayer.blend_space_x`
    - `AnimNode_ChooserPlayer.blend_space_y`
    - `AnimNode_ChooserPlayer.default_settings`