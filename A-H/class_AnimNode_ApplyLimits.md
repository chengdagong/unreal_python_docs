# unreal.AnimNode_ApplyLimits

```python
class unreal.AnimNode_ApplyLimits(component_pose:ComponentSpacePoseLink=\[\], lod_threshold:int=0, alpha_input_type:AnimAlphaInputType=Ellipsis, alpha_bool_enabled:bool=False, alpha:float=0.0, alpha_scale_bias:InputScaleBias=Ellipsis, alpha_bool_blend:InputAlphaBoolBlend=Ellipsis, alpha_curve_name:Name='None', alpha_scale_bias_clamp:InputScaleBiasClamp=Ellipsis, angular_offsets:None=\[\])
```


**Bases:** ``AnimNode_SkeletalControlBase``


Anim Node Apply Limits

**C++ Source:**

- **Module**: AnimGraphRuntime

- **File**: AnimNode\_ApplyLimits.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `alpha` (float): [Read-Write] Current strength of the skeletal control

- `alpha_bool_blend` (InputAlphaBoolBlend): [Read-Write]

- `alpha_bool_enabled` (bool): [Read-Write]

- `alpha_curve_name` (Name): [Read-Write]

- `alpha_input_type` (AnimAlphaInputType): [Read-Write]

- `alpha_scale_bias` (InputScaleBias): [Read-Write]

- `alpha_scale_bias_clamp` (InputScaleBiasClamp): [Read-Write]

- `angular_offsets` (Array[Vector]): [Read-Write]

- `angular_range_limits` (Array[AngularRangeLimit]): [Read-Write]

- `component_pose` (ComponentSpacePoseLink): [Read-Write] Input link

- `lod_threshold` (int32): [Read-Write] \* Max LOD that this node is allowed to run
\\* For example if you have LODThreshold to be 2, it will run until LOD 2 (based on 0 index)
\\* when the component LOD becomes 3, it will stop update/evaluate
\\* currently transition would be issue and that has to be re-visited



---

_property_ `angular_offsets`: None

[Read-Write]

**Type:**

( Array\ [Vector])

### Table of Contents

- `unreal.AnimNode_ApplyLimits`
  - `AnimNode_ApplyLimits`
    - `AnimNode_ApplyLimits.angular_offsets`