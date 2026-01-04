# unreal.AnimNode_CopyBone

```python
class unreal.AnimNode_CopyBone(component_pose:ComponentSpacePoseLink=\[\], lod_threshold:int=0, alpha_input_type:AnimAlphaInputType=Ellipsis, alpha_bool_enabled:bool=False, alpha:float=0.0, alpha_scale_bias:InputScaleBias=Ellipsis, alpha_bool_blend:InputAlphaBoolBlend=Ellipsis, alpha_curve_name:Name='None', alpha_scale_bias_clamp:InputScaleBiasClamp=Ellipsis, copy_translation:bool=False, copy_rotation:bool=False, copy_scale:bool=False)
```


**Bases:** ``AnimNode_SkeletalControlBase``


Simple controller to copy a bone’s transform to another one.

**C++ Source:**

- **Module**: AnimGraphRuntime

- **File**: AnimNode\_CopyBone.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `alpha` (float): [Read-Write] Current strength of the skeletal control

- `alpha_bool_blend` (InputAlphaBoolBlend): [Read-Write]

- `alpha_bool_enabled` (bool): [Read-Write]

- `alpha_curve_name` (Name): [Read-Write]

- `alpha_input_type` (AnimAlphaInputType): [Read-Write]

- `alpha_scale_bias` (InputScaleBias): [Read-Write]

- `alpha_scale_bias_clamp` (InputScaleBiasClamp): [Read-Write]

- `component_pose` (ComponentSpacePoseLink): [Read-Write] Input link

- `control_space` (BoneControlSpace): [Read-Write] Space to convert transforms into prior to copying components

- `copy_rotation` (bool): [Read-Write] If Rotation should be copied

- `copy_scale` (bool): [Read-Write] If Scale should be copied

- `copy_translation` (bool): [Read-Write] If Translation should be copied

- `lod_threshold` (int32): [Read-Write] \* Max LOD that this node is allowed to run
\\* For example if you have LODThreshold to be 2, it will run until LOD 2 (based on 0 index)
\\* when the component LOD becomes 3, it will stop update/evaluate
\\* currently transition would be issue and that has to be re-visited

- `source_bone` (BoneReference): [Read-Write] Source Bone Name to get transform from

- `target_bone` (BoneReference): [Read-Write] Name of bone to control. This is the main bone chain to modify from. \*



---

_property_ `copy_rotation`: bool

[Read-Write] If Rotation should be copied

**Type:**

( bool)


---

_property_ `copy_scale`: bool

[Read-Write] If Scale should be copied

**Type:**

( bool)


---

_property_ `copy_translation`: bool

[Read-Write] If Translation should be copied

**Type:**

( bool)

### Table of Contents

- `unreal.AnimNode_CopyBone`
  - `AnimNode_CopyBone`
    - `AnimNode_CopyBone.copy_rotation`
    - `AnimNode_CopyBone.copy_scale`
    - `AnimNode_CopyBone.copy_translation`