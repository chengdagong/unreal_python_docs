# unreal.AnimNode_OrientationWarping

```python
class unreal.AnimNode_OrientationWarping(component_pose:ComponentSpacePoseLink=\[\], lod_threshold:int=0, alpha_input_type:AnimAlphaInputType=Ellipsis, alpha_bool_enabled:bool=False, alpha:float=0.0, alpha_scale_bias:InputScaleBias=Ellipsis, alpha_bool_blend:InputAlphaBoolBlend=Ellipsis, alpha_curve_name:Name='None', alpha_scale_bias_clamp:InputScaleBiasClamp=Ellipsis, target_time:float=0.0, orientation_angle:float=0.0, locomotion_angle:float=0.0, locomotion_direction:Vector=Ellipsis, min_root_motion_speed_threshold:float=0.0, locomotion_angle_delta_threshold:float=0.0, current_anim_asset:AnimationAsset=Ellipsis, current_anim_asset_time:float=0.0, manual_root_motion_velocity:Vector=Ellipsis, warping_space:OrientationWarpingSpace=Ellipsis, warping_space_transform:Transform=Ellipsis)
```


**Bases:** ``AnimNode_SkeletalControlBase``


Maintains a look at direction for the upper body (orientation), while rotating the lower body to match capsule velocity direction
Does nothing if the root motion velocity direction matches the desired / current capsule velocity direction

**C++ Source:**

- **Plugin**: AnimationWarping

- **Module**: AnimationWarpingRuntime

- **File**: AnimNode\_OrientationWarping.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `alpha` (float): [Read-Write] Current strength of the skeletal control

- `alpha_bool_blend` (InputAlphaBoolBlend): [Read-Write]

- `alpha_bool_enabled` (bool): [Read-Write]

- `alpha_curve_name` (Name): [Read-Write]

- `alpha_input_type` (AnimAlphaInputType): [Read-Write]

- `alpha_scale_bias` (InputScaleBias): [Read-Write]

- `alpha_scale_bias_clamp` (InputScaleBiasClamp): [Read-Write]

- `component_pose` (ComponentSpacePoseLink): [Read-Write] Input link

- `counter_compensate_interp_speed` (float): [Read-Write] Same as RotationInterpSpeed, but for CounterCompensate smoothing. A value of 0 sample raw root motion.
Used to avoid stuttering from resampling root deltas. Root motion is already smooth, so a large value is our default (~75% of 60 fps).

- `counter_compenstate_interpolation_by_root_motion` (bool): [Read-Write] Whether to counter compensate interpolation by the animated root motion angle change over time.
This helps to conserve the motion from our animation.
Disable this if your root motion is expected to be jittery, and you want orientation warping to smooth it out.

- `current_anim_asset` (AnimationAsset): [Read-Write] Experimental. Animation Asset for incorporating root motion data. If ‘TargetTime’ is set, and the animation has root motion rotation within the TargetTime,
then those rotations will be scaled to reach the TargetOrientation

- `current_anim_asset_time` (float): [Read-Write] Experimental. Current playback time in seconds of the CurrentAnimAsset

- `debug_draw_scale` (float): [Read-Write] Scale all debug drawing visualization by a factor

- `distributed_bone_orientation_alpha` (float): [Read-Write] Specifies how much rotation is applied to the character body versus IK feet

- `enable_debug_draw` (bool): [Read-Write] Enable/Disable orientation warping debug drawing

- `ik_foot_bones` (Array[BoneReference]): [Read-Write] IK Foot definitions

- `ik_foot_root_bone` (BoneReference): [Read-Write] IK Foot Root Bone definition

- `locomotion_angle` (float): [Read-Write] The character locomotion angle (in degrees) relative to the specified RotationAxis
This will be used in the following equation for computing the orientation angle: [Orientation = RotationBetween(RootMotionDirection, LocomotionDirection)]
In most cases, this is the difference between the Velocity of the Movement Component and the actor rotation (obtained via CalculateDirection)

- `locomotion_angle_delta_threshold` (float): [Read-Write] Specifies an angle threshold to prevent erroneous over-rotation of the character, disabled with a value of 0

When the effective orientation warping angle is detected to be greater than this value (default: 90 degrees) the locomotion direction will be inverted prior to warping
This will be used in the following equation: [Orientation = RotationBetween(RootMotionDirection, -LocomotionDirection)]

Example: Playing a forward running animation while the motion is going backward
Rather than orientation warping by 180 degrees, the system will warp by 0 degrees

- `locomotion_direction` (Vector): [Read-Write] The character movement direction vector in world space
When set, this vector is used to compute LocomotionAngle automatically. When not set, the LocomotionAngle input should be used instead.
In most cases, this vector is the same as the Velocity vector of the Movement Component

- `lod_threshold` (int32): [Read-Write] \* Max LOD that this node is allowed to run
\\* For example if you have LODThreshold to be 2, it will run until LOD 2 (based on 0 index)
\\* when the component LOD becomes 3, it will stop update/evaluate
\\* currently transition would be issue and that has to be re-visited

- `manual_root_motion_velocity` (Vector): [Read-Write]

- `max_correction_degrees` (float): [Read-Write] Max correction we’re allowed to do per-second when using interpolation.
This minimizes pops when we have a large difference between current and target orientation.

- `max_root_motion_delta_to_compensate_degrees` (float): [Read-Write] Don’t compensate our interpolator when the instantaneous root motion delta is higher than this. This is likely a pivot.

- `min_root_motion_speed_threshold` (float): [Read-Write] Minimum root motion speed required to apply orientation warping
This is useful to prevent unnatural re-orientation when the animation has a portion with no root motion (i.e starts/stops/idles)
When this value is greater than 0, it’s recommended to enable interpolation with RotationInterpSpeed > 0

- `mode` (WarpingEvaluationMode): [Read-Write] Orientation warping evaluation mode (Graph or Manual)

- `orientation_angle` (float): [Read-Write] The desired orientation angle (in degrees) to warp by relative to the specified RotationAxis

- `rotation_axis` (AxisType): [Read-Write] Rotation axis used when rotating the character body

- `rotation_interp_speed` (float): [Read-Write] Specifies the interpolation speed (in Alpha per second) towards reaching the final warped rotation angle
A value of 0 will cause instantaneous rotation, while a greater value will introduce smoothing

- `scale_by_global_blend_weight` (bool): [Read-Write]

- `spine_bones` (Array[BoneReference]): [Read-Write] Spine bone definitions
Used to counter rotate the body in order to keep the character facing forward
The amount of counter rotation applied is driven by DistributedBoneOrientationAlpha

- `target_time` (float): [Read-Write] Experimental. Orientation warping should do nothing if root motion velocity directions match capsule,
however root motion can have multiple velocity directions. So we also check root motion
direction ‘TargetTime’ in the future for matching direction to avoid temp orientation warps.

- `use_manual_root_motion_velocity` (bool): [Read-Write]

- `warping_space` (OrientationWarpingSpace): [Read-Write]

- `warping_space_transform` (Transform): [Read-Write]



---

_property_ `current_anim_asset`: AnimationAsset

[Read-Write] Experimental. Animation Asset for incorporating root motion data. If ‘TargetTime’ is set, and the animation has root motion rotation within the TargetTime,
then those rotations will be scaled to reach the TargetOrientation

**Type:**

( AnimationAsset)


---

_property_ `current_anim_asset_time`: float

[Read-Write] Experimental. Current playback time in seconds of the CurrentAnimAsset

**Type:**

( float)


---

_property_ `locomotion_angle`: float

[Read-Write] The character locomotion angle (in degrees) relative to the specified RotationAxis
This will be used in the following equation for computing the orientation angle: [Orientation = RotationBetween(RootMotionDirection, LocomotionDirection)]
In most cases, this is the difference between the Velocity of the Movement Component and the actor rotation (obtained via CalculateDirection)

**Type:**

( float)


---

_property_ `locomotion_angle_delta_threshold`: float

[Read-Write] Specifies an angle threshold to prevent erroneous over-rotation of the character, disabled with a value of 0

When the effective orientation warping angle is detected to be greater than this value (default: 90 degrees) the locomotion direction will be inverted prior to warping
This will be used in the following equation: [Orientation = RotationBetween(RootMotionDirection, -LocomotionDirection)]

Example: Playing a forward running animation while the motion is going backward
Rather than orientation warping by 180 degrees, the system will warp by 0 degrees

**Type:**

( float)


---

_property_ `locomotion_direction`: Vector

[Read-Write] The character movement direction vector in world space
When set, this vector is used to compute LocomotionAngle automatically. When not set, the LocomotionAngle input should be used instead.
In most cases, this vector is the same as the Velocity vector of the Movement Component

**Type:**

( Vector)


---

_property_ `manual_root_motion_velocity`: Vector

[Read-Write]

**Type:**

( Vector)


---

_property_ `min_root_motion_speed_threshold`: float

[Read-Write] Minimum root motion speed required to apply orientation warping
This is useful to prevent unnatural re-orientation when the animation has a portion with no root motion (i.e starts/stops/idles)
When this value is greater than 0, it’s recommended to enable interpolation with RotationInterpSpeed > 0

**Type:**

( float)


---

_property_ `orientation_angle`: float

[Read-Write] The desired orientation angle (in degrees) to warp by relative to the specified RotationAxis

**Type:**

( float)


---

_property_ `target_time`: float

[Read-Write] Experimental. Orientation warping should do nothing if root motion velocity directions match capsule,
however root motion can have multiple velocity directions. So we also check root motion
direction ‘TargetTime’ in the future for matching direction to avoid temp orientation warps.

**Type:**

( float)


---

_property_ `warping_space`: OrientationWarpingSpace

[Read-Write]

**Type:**

( OrientationWarpingSpace)


---

_property_ `warping_space_transform`: Transform

[Read-Write]

**Type:**

( Transform)

### Table of Contents

- `unreal.AnimNode_OrientationWarping`
  - `AnimNode_OrientationWarping`
    - `AnimNode_OrientationWarping.current_anim_asset`
    - `AnimNode_OrientationWarping.current_anim_asset_time`
    - `AnimNode_OrientationWarping.locomotion_angle`
    - `AnimNode_OrientationWarping.locomotion_angle_delta_threshold`
    - `AnimNode_OrientationWarping.locomotion_direction`
    - `AnimNode_OrientationWarping.manual_root_motion_velocity`
    - `AnimNode_OrientationWarping.min_root_motion_speed_threshold`
    - `AnimNode_OrientationWarping.orientation_angle`
    - `AnimNode_OrientationWarping.target_time`
    - `AnimNode_OrientationWarping.warping_space`
    - `AnimNode_OrientationWarping.warping_space_transform`