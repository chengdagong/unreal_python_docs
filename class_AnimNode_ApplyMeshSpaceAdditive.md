# unreal.AnimNode_ApplyMeshSpaceAdditive

```python
class unreal.AnimNode_ApplyMeshSpaceAdditive(base:PoseLink=\[\], additive:PoseLink=\[\], root_space_additive:bool=False, alpha_input_type:AnimAlphaInputType=Ellipsis, alpha:float=0.0, alpha_bool_enabled:bool=False, alpha_bool_blend:InputAlphaBoolBlend=Ellipsis, alpha_curve_name:Name='None', alpha_scale_bias:InputScaleBias=Ellipsis, alpha_scale_bias_clamp:InputScaleBiasClamp=Ellipsis, lod_threshold:int=0)
```


**Bases:** ``AnimNode_Base``


Anim Node Apply Mesh Space Additive

**C++ Source:**

- **Module**: Engine

- **File**: AnimNode\_ApplyMeshSpaceAdditive.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `additive` (PoseLink): [Read-Write]

- `alpha` (float): [Read-Write] The float value that controls the alpha blending when the alpha input type is set to ‘Float’

- `alpha_bool_blend` (InputAlphaBoolBlend): [Read-Write]

- `alpha_bool_enabled` (bool): [Read-Write] The boolean value that controls the alpha blending when the alpha input type is set to ‘Bool’

- `alpha_curve_name` (Name): [Read-Write]

- `alpha_input_type` (AnimAlphaInputType): [Read-Write] The data type used to control the alpha blending of the additive pose.

Note: Changing this value will disconnect alpha input pins.

- `alpha_scale_bias` (InputScaleBias): [Read-Write]

- `alpha_scale_bias_clamp` (InputScaleBiasClamp): [Read-Write]

- `base` (PoseLink): [Read-Write]

- `lod_threshold` (int32): [Read-Write] \* Max LOD that this node is allowed to run
\\* For example if you have LODThreshold to be 2, it will run until LOD 2 (based on 0 index)
\\* when the component LOD becomes 3, it will stop update/evaluate
\\* currently transition would be issue and that has to be re-visited

- `root_space_additive` (bool): [Read-Write]



---

_property_ `additive`: PoseLink

[Read-Write]

**Type:**

( PoseLink)


---

_property_ `alpha`: float

[Read-Write] The float value that controls the alpha blending when the alpha input type is set to ‘Float’

**Type:**

( float)


---

_property_ `alpha_bool_blend`: InputAlphaBoolBlend

[Read-Write]

**Type:**

( InputAlphaBoolBlend)


---

_property_ `alpha_bool_enabled`: bool

[Read-Write] The boolean value that controls the alpha blending when the alpha input type is set to ‘Bool’

**Type:**

( bool)


---

_property_ `alpha_curve_name`: Name

[Read-Write]

**Type:**

( Name)


---

_property_ `alpha_input_type`: AnimAlphaInputType

[Read-Write] The data type used to control the alpha blending of the additive pose.
Note: Changing this value will disconnect alpha input pins.

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


---

_property_ `root_space_additive`: bool

[Read-Write]

**Type:**

( bool)

### Table of Contents

- `unreal.AnimNode_ApplyMeshSpaceAdditive`
  - `AnimNode_ApplyMeshSpaceAdditive`
    - `AnimNode_ApplyMeshSpaceAdditive.additive`
    - `AnimNode_ApplyMeshSpaceAdditive.alpha`
    - `AnimNode_ApplyMeshSpaceAdditive.alpha_bool_blend`
    - `AnimNode_ApplyMeshSpaceAdditive.alpha_bool_enabled`
    - `AnimNode_ApplyMeshSpaceAdditive.alpha_curve_name`
    - `AnimNode_ApplyMeshSpaceAdditive.alpha_input_type`
    - `AnimNode_ApplyMeshSpaceAdditive.alpha_scale_bias`
    - `AnimNode_ApplyMeshSpaceAdditive.alpha_scale_bias_clamp`
    - `AnimNode_ApplyMeshSpaceAdditive.base`
    - `AnimNode_ApplyMeshSpaceAdditive.lod_threshold`
    - `AnimNode_ApplyMeshSpaceAdditive.root_space_additive`