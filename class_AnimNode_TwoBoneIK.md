# unreal.AnimNode_TwoBoneIK

```python
class unreal.AnimNode_TwoBoneIK(component_pose:ComponentSpacePoseLink=\[\], lod_threshold:int=0, alpha_input_type:AnimAlphaInputType=Ellipsis, alpha_bool_enabled:bool=False, alpha:float=0.0, alpha_scale_bias:InputScaleBias=Ellipsis, alpha_bool_blend:InputAlphaBoolBlend=Ellipsis, alpha_curve_name:Name='None', alpha_scale_bias_clamp:InputScaleBiasClamp=Ellipsis, effector_location:Vector=Ellipsis, joint_target_location:Vector=Ellipsis)
```


**Bases:** ``AnimNode_SkeletalControlBase``


Simple 2 Bone IK Controller.

**C++ Source:**

- **Module**: AnimGraphRuntime

- **File**: AnimNode\_TwoBoneIK.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `allow_stretching` (bool): [Read-Write] Should stretching be allowed, to be prevent over extension

- `allow_twist` (bool): [Read-Write] Whether or not to apply twist on the chain of joints. This clears the twist value along the TwistAxis

- `alpha` (float): [Read-Write] Current strength of the skeletal control

- `alpha_bool_blend` (InputAlphaBoolBlend): [Read-Write]

- `alpha_bool_enabled` (bool): [Read-Write]

- `alpha_curve_name` (Name): [Read-Write]

- `alpha_input_type` (AnimAlphaInputType): [Read-Write]

- `alpha_scale_bias` (InputScaleBias): [Read-Write]

- `alpha_scale_bias_clamp` (InputScaleBiasClamp): [Read-Write]

- `component_pose` (ComponentSpacePoseLink): [Read-Write] Input link

- `effector_location` (Vector): [Read-Write] Effector Location. Target Location to reach.

- `effector_location_space` (BoneControlSpace): [Read-Write] Reference frame of Effector Location.

- `effector_target` (BoneSocketTarget): [Read-Write]

- `ik_bone` (BoneReference): [Read-Write] Name of bone to control. This is the main bone chain to modify from. \*

- `joint_target` (BoneSocketTarget): [Read-Write]

- `joint_target_location` (Vector): [Read-Write] Joint Target Location. Location used to orient Joint bone. \*

- `joint_target_location_space` (BoneControlSpace): [Read-Write] Reference frame of Joint Target Location.

- `lod_threshold` (int32): [Read-Write] \* Max LOD that this node is allowed to run
\\* For example if you have LODThreshold to be 2, it will run until LOD 2 (based on 0 index)
\\* when the component LOD becomes 3, it will stop update/evaluate
\\* currently transition would be issue and that has to be re-visited

- `maintain_effector_rel_rot` (bool): [Read-Write] Keep local rotation of end bone

- `max_stretch_scale` (double): [Read-Write] Limits to use if stretching is allowed. This value determins what is the max stretch scale. For example, 1.5 means it will stretch until 150 % of the whole length of the limb.

- `start_stretch_ratio` (double): [Read-Write] Limits to use if stretching is allowed. This value determines when to start stretch. For example, 0.9 means once it reaches 90% of the whole length of the limb, it will start apply.

- `take_rotation_from_effector_space` (bool): [Read-Write] Set end bone to use End Effector rotation

- `twist_axis` (Axis): [Read-Write] Specify which axis it’s aligned. Used when removing twist



---

_property_ `effector_location`: Vector

[Read-Write] Effector Location. Target Location to reach.

**Type:**

( Vector)


---

_property_ `joint_target_location`: Vector

[Read-Write] Joint Target Location. Location used to orient Joint bone. \*

**Type:**

( Vector)

### Table of Contents

- `unreal.AnimNode_TwoBoneIK`
  - `AnimNode_TwoBoneIK`
    - `AnimNode_TwoBoneIK.effector_location`
    - `AnimNode_TwoBoneIK.joint_target_location`