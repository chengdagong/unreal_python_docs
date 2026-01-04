# unreal.AnimNode_ApplyAdditive

```python
class unreal.AnimNode_ApplyAdditive(base:PoseLink=\[\], additive:PoseLink=\[\], alpha:float=0.0, alpha_scale_bias:InputScaleBias=Ellipsis, lod_threshold:int=0, alpha_bool_blend:InputAlphaBoolBlend=Ellipsis, alpha_curve_name:Name='None', alpha_scale_bias_clamp:InputScaleBiasClamp=Ellipsis, alpha_input_type:AnimAlphaInputType=Ellipsis, alpha_bool_enabled:bool=False)
```


**Bases:** ``AnimNode_Base``


Anim Node Apply Additive

**C++ Source:**

- **Module**: AnimGraphRuntime

- **File**: AnimNode\_ApplyAdditive.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `additive` (PoseLink): [Read-Write]

- `alpha` (float): [Read-Write]

- `alpha_bool_blend` (InputAlphaBoolBlend): [Read-Write]

- `alpha_bool_enabled` (bool): [Read-Write]

- `alpha_curve_name` (Name): [Read-Write]

- `alpha_input_type` (AnimAlphaInputType): [Read-Write]

- `alpha_scale_bias` (InputScaleBias): [Read-Write]

- `alpha_scale_bias_clamp` (InputScaleBiasClamp): [Read-Write]

- `base` (PoseLink): [Read-Write]

- `lod_threshold` (int32): [Read-Write] \* Max LOD that this node is allowed to run
\\* For example if you have LODThreshold to be 2, it will run until LOD 2 (based on 0 index)
\\* when the component LOD becomes 3, it will stop update/evaluate
\\* currently transition would be issue and that has to be re-visited



---

_property_ `additive`: PoseLink

[Read-Write]

**Type:**

( PoseLink)


---

_property_ `alpha`: float

[Read-Write]

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

_property_ `base`: PoseLink

[Read-Write]

**Type:**

( PoseLink)


---

_property_ `lod_threshold`: int

[Read-Write] \* Max LOD that this node is allowed to run
\\* For example if you have LODThreshold to be 2, it will run until LOD 2 (based on 0 index)
\\* when the component LOD becomes 3, it will stop update/evaluate
\\* currently transition would be issue and that has to be re-visited

**Type:**

(int32)

### Table of Contents

- `unreal.AnimNode_ApplyAdditive`
  - `AnimNode_ApplyAdditive`
    - `AnimNode_ApplyAdditive.additive`
    - `AnimNode_ApplyAdditive.alpha`
    - `AnimNode_ApplyAdditive.alpha_bool_blend`
    - `AnimNode_ApplyAdditive.alpha_bool_enabled`
    - `AnimNode_ApplyAdditive.alpha_curve_name`
    - `AnimNode_ApplyAdditive.alpha_input_type`
    - `AnimNode_ApplyAdditive.alpha_scale_bias`
    - `AnimNode_ApplyAdditive.alpha_scale_bias_clamp`
    - `AnimNode_ApplyAdditive.base`
    - `AnimNode_ApplyAdditive.lod_threshold`