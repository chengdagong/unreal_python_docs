# unreal.AnimNode_RotationMultiplier

```python
class unreal.AnimNode_RotationMultiplier(component_pose:ComponentSpacePoseLink=\[\], lod_threshold:int=0, alpha_input_type:AnimAlphaInputType=Ellipsis, alpha_bool_enabled:bool=False, alpha:float=0.0, alpha_scale_bias:InputScaleBias=Ellipsis, alpha_bool_blend:InputAlphaBoolBlend=Ellipsis, alpha_curve_name:Name='None', alpha_scale_bias_clamp:InputScaleBiasClamp=Ellipsis, multiplier:float=0.0)
```


**Bases:** ``AnimNode_SkeletalControlBase``


Simple controller that multiplies scalar value to the translation/rotation/scale of a single bone.

**C++ Source:**

- **Module**: AnimGraphRuntime

- **File**: AnimNode\_RotationMultiplier.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `alpha` (float): [Read-Write] Current strength of the skeletal control

- `alpha_bool_blend` (InputAlphaBoolBlend): [Read-Write]

- `alpha_bool_enabled` (bool): [Read-Write]

- `alpha_curve_name` (Name): [Read-Write]

- `alpha_input_type` (AnimAlphaInputType): [Read-Write]

- `alpha_scale_bias` (InputScaleBias): [Read-Write]

- `alpha_scale_bias_clamp` (InputScaleBiasClamp): [Read-Write]

- `component_pose` (ComponentSpacePoseLink): [Read-Write] Input link

- `is_additive` (bool): [Read-Write]

- `lod_threshold` (int32): [Read-Write] \* Max LOD that this node is allowed to run
\\* For example if you have LODThreshold to be 2, it will run until LOD 2 (based on 0 index)
\\* when the component LOD becomes 3, it will stop update/evaluate
\\* currently transition would be issue and that has to be re-visited

- `multiplier` (float): [Read-Write] To make these to be easily pin-hookable, I’m not making it struct, but each variable
0.f is invalid, and default

- `rotation_axis_to_refer` (BoneAxis): [Read-Write]

- `source_bone` (BoneReference): [Read-Write] Source to get transform from

- `target_bone` (BoneReference): [Read-Write] Name of bone to control. This is the main bone chain to modify from.



---

_property_ `multiplier`: float

[Read-Write] To make these to be easily pin-hookable, I’m not making it struct, but each variable
0.f is invalid, and default

**Type:**

( float)

### Table of Contents

- `unreal.AnimNode_RotationMultiplier`
  - `AnimNode_RotationMultiplier`
    - `AnimNode_RotationMultiplier.multiplier`