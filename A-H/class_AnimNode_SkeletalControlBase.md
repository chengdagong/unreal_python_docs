# unreal.AnimNode_SkeletalControlBase

```python
class unreal.AnimNode_SkeletalControlBase(component_pose:ComponentSpacePoseLink=\[\], lod_threshold:int=0, alpha_input_type:AnimAlphaInputType=Ellipsis, alpha_bool_enabled:bool=False, alpha:float=0.0, alpha_scale_bias:InputScaleBias=Ellipsis, alpha_bool_blend:InputAlphaBoolBlend=Ellipsis, alpha_curve_name:Name='None', alpha_scale_bias_clamp:InputScaleBiasClamp=Ellipsis)
```


**Bases:** ``AnimNode_Base``


Anim Node Skeletal Control Base

**C++ Source:**

- **Module**: AnimGraphRuntime

- **File**: AnimNode\_SkeletalControlBase.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `alpha` (float): [Read-Write] Current strength of the skeletal control

- `alpha_bool_blend` (InputAlphaBoolBlend): [Read-Write]

- `alpha_bool_enabled` (bool): [Read-Write]

- `alpha_curve_name` (Name): [Read-Write]

- `alpha_input_type` (AnimAlphaInputType): [Read-Write]

- `alpha_scale_bias` (InputScaleBias): [Read-Write]

- `alpha_scale_bias_clamp` (InputScaleBiasClamp): [Read-Write]

- `component_pose` (ComponentSpacePoseLink): [Read-Write] Input link

- `lod_threshold` (int32): [Read-Write] \* Max LOD that this node is allowed to run
\\* For example if you have LODThreshold to be 2, it will run until LOD 2 (based on 0 index)
\\* when the component LOD becomes 3, it will stop update/evaluate
\\* currently transition would be issue and that has to be re-visited



---

_property_ `alpha`: float

[Read-Write] Current strength of the skeletal control

**Type:**

( float)


---

_property_ `alpha_bool_blend`: InputAlphaBoolBlend

[Read-Write]

**Type:**

( InputAlphaBoolBlend)


---

_property_ `alpha_bool_enabled`: bool

[Read-Write]

**Type:**

( bool)


---

_property_ `alpha_curve_name`: Name

[Read-Write]

**Type:**

( Name)


---

_property_ `alpha_input_type`: AnimAlphaInputType

[Read-Write]

**Type:**

( AnimAlphaInputType)


---

_property_ `alpha_scale_bias`: InputScaleBias

[Read-Write]

**Type:**

( InputScaleBias)


---

_property_ `alpha_scale_bias_clamp`: InputScaleBiasClamp

[Read-Write]

**Type:**

( InputScaleBiasClamp)


---

_property_ `component_pose`: ComponentSpacePoseLink

[Read-Write] Input link

**Type:**

( ComponentSpacePoseLink)


---

_property_ `lod_threshold`: int

[Read-Write] \* Max LOD that this node is allowed to run
\\* For example if you have LODThreshold to be 2, it will run until LOD 2 (based on 0 index)
\\* when the component LOD becomes 3, it will stop update/evaluate
\\* currently transition would be issue and that has to be re-visited

**Type:**

(int32)

### Table of Contents

- `unreal.AnimNode_SkeletalControlBase`
  - `AnimNode_SkeletalControlBase`
    - `AnimNode_SkeletalControlBase.alpha`
    - `AnimNode_SkeletalControlBase.alpha_bool_blend`
    - `AnimNode_SkeletalControlBase.alpha_bool_enabled`
    - `AnimNode_SkeletalControlBase.alpha_curve_name`
    - `AnimNode_SkeletalControlBase.alpha_input_type`
    - `AnimNode_SkeletalControlBase.alpha_scale_bias`
    - `AnimNode_SkeletalControlBase.alpha_scale_bias_clamp`
    - `AnimNode_SkeletalControlBase.component_pose`
    - `AnimNode_SkeletalControlBase.lod_threshold`