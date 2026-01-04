# unreal.AnimNode_CopyBoneDelta

```python
class unreal.AnimNode_CopyBoneDelta(component_pose:ComponentSpacePoseLink=\[\], lod_threshold:int=0, alpha_input_type:AnimAlphaInputType=Ellipsis, alpha_bool_enabled:bool=False, alpha:float=0.0, alpha_scale_bias:InputScaleBias=Ellipsis, alpha_bool_blend:InputAlphaBoolBlend=Ellipsis, alpha_curve_name:Name='None', alpha_scale_bias_clamp:InputScaleBiasClamp=Ellipsis, copy_translation:bool=False, copy_rotation:bool=False, copy_scale:bool=False, translation_multiplier:float=0.0, rotation_multiplier:float=0.0, scale_multiplier:float=0.0)
```


**Bases:** ``AnimNode_SkeletalControlBase``


Simple controller to copy a transform relative to the ref pose to the target bone,
instead of the copy bone node which copies the absolute transform

**C++ Source:**

- **Module**: AnimGraphRuntime

- **File**: AnimNode\_CopyBoneDelta.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `alpha` (float): [Read-Write] Current strength of the skeletal control

- `alpha_bool_blend` (InputAlphaBoolBlend): [Read-Write]

- `alpha_bool_enabled` (bool): [Read-Write]

- `alpha_curve_name` (Name): [Read-Write]

- `alpha_input_type` (AnimAlphaInputType): [Read-Write]

- `alpha_scale_bias` (InputScaleBias): [Read-Write]

- `alpha_scale_bias_clamp` (InputScaleBiasClamp): [Read-Write]

- `component_pose` (ComponentSpacePoseLink): [Read-Write] Input link

- `copy_mode` (CopyBoneDeltaMode): [Read-Write]

- `copy_rotation` (bool): [Read-Write]

- `copy_scale` (bool): [Read-Write]

- `copy_translation` (bool): [Read-Write]

- `lod_threshold` (int32): [Read-Write] \* Max LOD that this node is allowed to run
\\* For example if you have LODThreshold to be 2, it will run until LOD 2 (based on 0 index)
\\* when the component LOD becomes 3, it will stop update/evaluate
\\* currently transition would be issue and that has to be re-visited

- `rotation_multiplier` (float): [Read-Write]

- `scale_multiplier` (float): [Read-Write]

- `source_bone` (BoneReference): [Read-Write]

- `target_bone` (BoneReference): [Read-Write]

- `translation_multiplier` (float): [Read-Write]



---

_property_ `copy_rotation`: bool

[Read-Write]

**Type:**

( bool)


---

_property_ `copy_scale`: bool

[Read-Write]

**Type:**

( bool)


---

_property_ `copy_translation`: bool

[Read-Write]

**Type:**

( bool)


---

_property_ `rotation_multiplier`: float

[Read-Write]

**Type:**

( float)


---

_property_ `scale_multiplier`: float

[Read-Write]

**Type:**

( float)


---

_property_ `translation_multiplier`: float

[Read-Write]

**Type:**

( float)

### Table of Contents

- `unreal.AnimNode_CopyBoneDelta`
  - `AnimNode_CopyBoneDelta`
    - `AnimNode_CopyBoneDelta.copy_rotation`
    - `AnimNode_CopyBoneDelta.copy_scale`
    - `AnimNode_CopyBoneDelta.copy_translation`
    - `AnimNode_CopyBoneDelta.rotation_multiplier`
    - `AnimNode_CopyBoneDelta.scale_multiplier`
    - `AnimNode_CopyBoneDelta.translation_multiplier`