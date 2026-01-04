# unreal.AnimNode_StrideWarping

```python
class unreal.AnimNode_StrideWarping(component_pose:ComponentSpacePoseLink=\[\], lod_threshold:int=0, alpha_input_type:AnimAlphaInputType=Ellipsis, alpha_bool_enabled:bool=False, alpha:float=0.0, alpha_scale_bias:InputScaleBias=Ellipsis, alpha_bool_blend:InputAlphaBoolBlend=Ellipsis, alpha_curve_name:Name='None', alpha_scale_bias_clamp:InputScaleBiasClamp=Ellipsis, stride_direction:Vector=Ellipsis, stride_scale:float=0.0, locomotion_speed:float=0.0, min_root_motion_speed_threshold:float=0.0, floor_normal_direction:WarpingVectorValue=Ellipsis, gravity_direction:WarpingVectorValue=Ellipsis)
```


**Bases:** ``AnimNode_SkeletalControlBase``


Anim Node Stride Warping

**C++ Source:**

- **Plugin**: AnimationWarping

- **Module**: AnimationWarpingRuntime

- **File**: AnimNode\_StrideWarping.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `alpha` (float): [Read-Write] Current strength of the skeletal control

- `alpha_bool_blend` (InputAlphaBoolBlend): [Read-Write]

- `alpha_bool_enabled` (bool): [Read-Write]

- `alpha_curve_name` (Name): [Read-Write]

- `alpha_input_type` (AnimAlphaInputType): [Read-Write]

- `alpha_scale_bias` (InputScaleBias): [Read-Write]

- `alpha_scale_bias_clamp` (InputScaleBiasClamp): [Read-Write]

- `clamp_ik_using_fk_limits` (bool): [Read-Write] Clamps the IK foot warping to prevent over-extension relative to the overall FK leg

- `compensate_ik_using_fk_thigh_rotation` (bool): [Read-Write] Include warping adjustment to the FK thigh bones alongside the IK/FK foot definitions
This is used to help preserve the original overall leg shape

- `component_pose` (ComponentSpacePoseLink): [Read-Write] Input link

- `debug_draw_ik_foot_adjustment` (bool): [Read-Write] Enable/Disable IK foot location debug drawing following initial foot adjustment

- `debug_draw_ik_foot_final` (bool): [Read-Write] Enable/Disable IK foot location debug drawing following all adsjustments (Final warped result)

- `debug_draw_ik_foot_origin` (bool): [Read-Write] Enable/Disable IK foot location debug drawing prior to warping

- `debug_draw_pelvis_adjustment` (bool): [Read-Write] Enable/Disable pelvis debug drawing following adjustment

- `debug_draw_scale` (float): [Read-Write] Scale all debug drawing visualization by a factor

- `debug_draw_thigh_adjustment` (bool): [Read-Write] Enable/Disable thigh debug drawing following adjustment

- `disable_if_missing_root_motion` (bool): [Read-Write] Do not execute stride warping if animation data has no root motion

- `enable_debug_draw` (bool): [Read-Write] Enable/Disable stride warping debug drawing

- `floor_normal_direction` (WarpingVectorValue): [Read-Write] Floor normal direction, this value will internally convert into a corresponding Component-space representation prior to warping
Default: World Space, Up Vector: <0,0,1>

- `foot_definitions` (Array[StrideWarpingFootDefinition]): [Read-Write] Foot definitions specifying the IK, FK, and Thigh bone

- `gravity_direction` (WarpingVectorValue): [Read-Write] Gravity direction, this value will internally convert into a corresponding Component-space representation prior to warping
Default: World Space, Down Vector: <0,0,-1>

- `ik_foot_root_bone` (BoneReference): [Read-Write] IK Foot Root Bone definition

- `locomotion_speed` (float): [Read-Write] Locomotion speed, specifying the current speed of the character
This will be used in the following equation for computing the stride scale: [StrideScale = (LocomotionSpeed / RootMotionSpeed)]
Note: This speed should be relative to the delta time of the animation graph

Stride scale is a value specifying the amount of warping applied to the IK foot definitions
Example: A value of 0.5 will decrease the effective leg stride by half, while a value of 2.0 will double it

- `lod_threshold` (int32): [Read-Write] \* Max LOD that this node is allowed to run
\\* For example if you have LODThreshold to be 2, it will run until LOD 2 (based on 0 index)
\\* when the component LOD becomes 3, it will stop update/evaluate
\\* currently transition would be issue and that has to be re-visited

- `min_root_motion_speed_threshold` (float): [Read-Write] Minimum root motion speed required to apply stride warping
This is useful to prevent unnatural strides when the animation has a portion with no root motion (i.e starts/stops)
When this value is greater than 0, it’s recommended to enable interpolation in StrideScaleModifier

- `mode` (WarpingEvaluationMode): [Read-Write] Stride warping evaluation mode (Graph or Manual)

- `orient_stride_direction_using_floor_normal` (bool): [Read-Write] Orients the specified (Manual) or computed (Graph) stride direction by the floor normal

- `pelvis_bone` (BoneReference): [Read-Write] Pevlis Bone definition

- `pelvis_ik_foot_solver` (IKFootPelvisPullDownSolver): [Read-Write] Solver for controlling how much the pelvis is “pulled down” towards the IK/FK foot definitions during leg limb extension

- `stride_direction` (Vector): [Read-Write] Component-space stride direction
Example: A value of <1,0,0> will warp the leg stride along the Forward Vector

- `stride_scale` (float): [Read-Write] Stride scale, specifying the amount of warping applied to the foot definitions
Example: A value of 0.5 will decrease the effective leg stride by half, while a value of 2.0 will double it

- `stride_scale_modifier` (InputClampConstants): [Read-Write] Modifies the final stride scale value by optionally clamping and/or interpolating



---

_property_ `floor_normal_direction`: WarpingVectorValue

[Read-Write] Floor normal direction, this value will internally convert into a corresponding Component-space representation prior to warping
Default: World Space, Up Vector: <0,0,1>

**Type:**

( WarpingVectorValue)


---

_property_ `gravity_direction`: WarpingVectorValue

[Read-Write] Gravity direction, this value will internally convert into a corresponding Component-space representation prior to warping
Default: World Space, Down Vector: <0,0,-1>

**Type:**

( WarpingVectorValue)


---

_property_ `locomotion_speed`: float

[Read-Write] Locomotion speed, specifying the current speed of the character
This will be used in the following equation for computing the stride scale: [StrideScale = (LocomotionSpeed / RootMotionSpeed)]
Note: This speed should be relative to the delta time of the animation graph

Stride scale is a value specifying the amount of warping applied to the IK foot definitions
Example: A value of 0.5 will decrease the effective leg stride by half, while a value of 2.0 will double it

**Type:**

( float)


---

_property_ `min_root_motion_speed_threshold`: float

[Read-Write] Minimum root motion speed required to apply stride warping
This is useful to prevent unnatural strides when the animation has a portion with no root motion (i.e starts/stops)
When this value is greater than 0, it’s recommended to enable interpolation in StrideScaleModifier

**Type:**

( float)


---

_property_ `stride_direction`: Vector

[Read-Write] Component-space stride direction
Example: A value of <1,0,0> will warp the leg stride along the Forward Vector

**Type:**

( Vector)


---

_property_ `stride_scale`: float

[Read-Write] Stride scale, specifying the amount of warping applied to the foot definitions
Example: A value of 0.5 will decrease the effective leg stride by half, while a value of 2.0 will double it

**Type:**

( float)

### Table of Contents

- `unreal.AnimNode_StrideWarping`
  - `AnimNode_StrideWarping`
    - `AnimNode_StrideWarping.floor_normal_direction`
    - `AnimNode_StrideWarping.gravity_direction`
    - `AnimNode_StrideWarping.locomotion_speed`
    - `AnimNode_StrideWarping.min_root_motion_speed_threshold`
    - `AnimNode_StrideWarping.stride_direction`
    - `AnimNode_StrideWarping.stride_scale`