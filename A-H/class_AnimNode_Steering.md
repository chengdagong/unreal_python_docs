# unreal.AnimNode_Steering

```python
class unreal.AnimNode_Steering(component_pose:ComponentSpacePoseLink=\[\], lod_threshold:int=0, alpha_input_type:AnimAlphaInputType=Ellipsis, alpha_bool_enabled:bool=False, alpha:float=0.0, alpha_scale_bias:InputScaleBias=Ellipsis, alpha_bool_blend:InputAlphaBoolBlend=Ellipsis, alpha_curve_name:Name='None', alpha_scale_bias_clamp:InputScaleBiasClamp=Ellipsis, target_orientation:Quat=Ellipsis, mirrored:bool=False, procedural_target_time:float=0.0, animated_target_time:float=0.0, mirror_data_table:MirrorDataTable=Ellipsis, current_anim_asset:AnimationAsset=Ellipsis, current_anim_asset_time:float=0.0)
```


**Bases:** ``AnimNode_SkeletalControlBase``


Add procedural delta to the root motion attribute
This is done via 2 techniques:

> 1. Scaling the root motion on an animation
>
> 2. Adding additional correction to root motion after accounting for the anticipated (potentially scaled) root motion

The effects of 1) and 2) combine

**C++ Source:**

- **Plugin**: AnimationWarping

- **Module**: AnimationWarpingRuntime

- **File**: AnimNode\_Steering.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `alpha` (float): [Read-Write] Current strength of the skeletal control

- `alpha_bool_blend` (InputAlphaBoolBlend): [Read-Write]

- `alpha_bool_enabled` (bool): [Read-Write]

- `alpha_curve_name` (Name): [Read-Write]

- `alpha_input_type` (AnimAlphaInputType): [Read-Write]

- `alpha_scale_bias` (InputScaleBias): [Read-Write]

- `alpha_scale_bias_clamp` (InputScaleBiasClamp): [Read-Write]

- `animated_target_time` (float): [Read-Write] The number of seconds in the future to sample the root motion to know how much this animation is expected to turn

- `component_pose` (ComponentSpacePoseLink): [Read-Write] Input link

- `current_anim_asset` (AnimationAsset): [Read-Write] Animation Asset for incorporating root motion data. If CurrentAnimAsset is set, and the animation has root motion rotation within the TargetTime, then those rotations will be scaled to reach the TargetOrientation

- `current_anim_asset_time` (float): [Read-Write] Current playback time in seconds of the CurrentAnimAsset

- `disable_additive_below_speed` (float): [Read-Write] below this movement speed (based on the root motion in the animation) disable steering coming from the additive spring based correction

- `disable_steering_below_speed` (float): [Read-Write] below this movement speed (based on the root motion in the animation) disable steering completely (both scaling and additive)

- `lod_threshold` (int32): [Read-Write] \* Max LOD that this node is allowed to run
\\* For example if you have LODThreshold to be 2, it will run until LOD 2 (based on 0 index)
\\* when the component LOD becomes 3, it will stop update/evaluate
\\* currently transition would be issue and that has to be re-visited

- `max_scale_ratio` (float): [Read-Write] Will clamp the scaling ratio applied to below this threshold. Any error remaining will be compensated for linearly (using ProceduralTargetTime)

- `min_scale_ratio` (float): [Read-Write] Will clamp the scaling ratio applied to above this threshold. Any error remaining will be compensated for linearly (using ProceduralTargetTime)

- `mirror_data_table` (MirrorDataTable): [Read-Write] If bMirrored is set, MirrorDataTable will be used for mirroring the CurrentAnimAsset during prediction

- `mirrored` (bool): [Read-Write] True if input animation is mirrored

- `procedural_target_time` (float): [Read-Write] The number of seconds in the future before we should roughly attempt reach the TargetOrientation via additive correction

- `root_motion_threshold` (float): [Read-Write] The minimum amount of root motion required to enable root motion scaling.
The root motion is measured from current time to AnimatedTargetTime

- `target_orientation` (Quat): [Read-Write] The Orientation to steer towards

- `target_time` (float): [Read-Write]
deprecated: Use Procedural target time for the correction time scale and AnimatedTargetTime for the look ahead time on the animation



---

_property_ `animated_target_time`: float

[Read-Write] The number of seconds in the future to sample the root motion to know how much this animation is expected to turn

**Type:**

( float)


---

_property_ `current_anim_asset`: AnimationAsset

[Read-Write] Animation Asset for incorporating root motion data. If CurrentAnimAsset is set, and the animation has root motion rotation within the TargetTime, then those rotations will be scaled to reach the TargetOrientation

**Type:**

( AnimationAsset)


---

_property_ `current_anim_asset_time`: float

[Read-Write] Current playback time in seconds of the CurrentAnimAsset

**Type:**

( float)


---

_property_ `mirror_data_table`: MirrorDataTable

[Read-Write] If bMirrored is set, MirrorDataTable will be used for mirroring the CurrentAnimAsset during prediction

**Type:**

( MirrorDataTable)


---

_property_ `mirrored`: bool

[Read-Write] True if input animation is mirrored

**Type:**

( bool)


---

_property_ `procedural_target_time`: float

[Read-Write] The number of seconds in the future before we should roughly attempt reach the TargetOrientation via additive correction

**Type:**

( float)


---

_property_ `target_orientation`: Quat

[Read-Write] The Orientation to steer towards

**Type:**

( Quat)


---

_property_ `target_time`: float

[Read-Write]
deprecated: Use Procedural target time for the correction time scale and AnimatedTargetTime for the look ahead time on the animation

**Type:**

( float)

### Table of Contents

- `unreal.AnimNode_Steering`
  - `AnimNode_Steering`
    - `AnimNode_Steering.animated_target_time`
    - `AnimNode_Steering.current_anim_asset`
    - `AnimNode_Steering.current_anim_asset_time`
    - `AnimNode_Steering.mirror_data_table`
    - `AnimNode_Steering.mirrored`
    - `AnimNode_Steering.procedural_target_time`
    - `AnimNode_Steering.target_orientation`
    - `AnimNode_Steering.target_time`