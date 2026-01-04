# unreal.AnimNode_LookAt

```python
class unreal.AnimNode_LookAt(component_pose:ComponentSpacePoseLink=\[\], lod_threshold:int=0, alpha_input_type:AnimAlphaInputType=Ellipsis, alpha_bool_enabled:bool=False, alpha:float=0.0, alpha_scale_bias:InputScaleBias=Ellipsis, alpha_bool_blend:InputAlphaBoolBlend=Ellipsis, alpha_curve_name:Name='None', alpha_scale_bias_clamp:InputScaleBiasClamp=Ellipsis, look_at_location:Vector=Ellipsis, interpolation_type:InterpolationBlend=Ellipsis, look_at_clamp:float=0.0, interpolation_time:float=0.0, interpolation_trigger_threashold:float=0.0)
```


**Bases:** ``AnimNode_SkeletalControlBase``


Simple controller that make a bone to look at the point or another bone

**C++ Source:**

- **Module**: AnimGraphRuntime

- **File**: AnimNode\_LookAt.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `alpha` (float): [Read-Write] Current strength of the skeletal control

- `alpha_bool_blend` (InputAlphaBoolBlend): [Read-Write]

- `alpha_bool_enabled` (bool): [Read-Write]

- `alpha_curve_name` (Name): [Read-Write]

- `alpha_input_type` (AnimAlphaInputType): [Read-Write]

- `alpha_scale_bias` (InputScaleBias): [Read-Write]

- `alpha_scale_bias_clamp` (InputScaleBiasClamp): [Read-Write]

- `bone_to_modify` (BoneReference): [Read-Write] Name of bone to control. This is the main bone chain to modify from. \*

- `component_pose` (ComponentSpacePoseLink): [Read-Write] Input link

- `interpolation_time` (float): [Read-Write]

- `interpolation_trigger_threashold` (float): [Read-Write]

- `interpolation_type` (InterpolationBlend): [Read-Write]

- `lod_threshold` (int32): [Read-Write] \* Max LOD that this node is allowed to run
\\* For example if you have LODThreshold to be 2, it will run until LOD 2 (based on 0 index)
\\* when the component LOD becomes 3, it will stop update/evaluate
\\* currently transition would be issue and that has to be re-visited

- `look_at_axis` (Axis): [Read-Write]

- `look_at_clamp` (float): [Read-Write] Look at Clamp value in degrees - if your look at axis is Z, only X, Y degree of clamp will be used

- `look_at_location` (Vector): [Read-Write] Target Offset. It’s in world space if LookAtBone is empty or it is based on LookAtBone or LookAtSocket in their local space

- `look_at_target` (BoneSocketTarget): [Read-Write] Target socket to look at. Used if LookAtBone is empty. - You can use LookAtLocation if you need offset from this point. That location will be used in their local space. \*

- `look_up_axis` (Axis): [Read-Write]

- `use_look_up_axis` (bool): [Read-Write] Whether or not to use Look up axis



---

_property_ `interpolation_time`: float

[Read-Write]

**Type:**

( float)


---

_property_ `interpolation_trigger_threashold`: float

[Read-Write]

**Type:**

( float)


---

_property_ `interpolation_type`: InterpolationBlend

[Read-Write]

**Type:**

( InterpolationBlend)


---

_property_ `look_at_clamp`: float

[Read-Write] Look at Clamp value in degrees - if your look at axis is Z, only X, Y degree of clamp will be used

**Type:**

( float)


---

_property_ `look_at_location`: Vector

[Read-Write] Target Offset. It’s in world space if LookAtBone is empty or it is based on LookAtBone or LookAtSocket in their local space

**Type:**

( Vector)

### Table of Contents

- `unreal.AnimNode_LookAt`
  - `AnimNode_LookAt`
    - `AnimNode_LookAt.interpolation_time`
    - `AnimNode_LookAt.interpolation_trigger_threashold`
    - `AnimNode_LookAt.interpolation_type`
    - `AnimNode_LookAt.look_at_clamp`
    - `AnimNode_LookAt.look_at_location`