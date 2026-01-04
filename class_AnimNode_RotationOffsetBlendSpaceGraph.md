# unreal.AnimNode_RotationOffsetBlendSpaceGraph

```python
class unreal.AnimNode_RotationOffsetBlendSpaceGraph(x:float=0.0, y:float=0.0, group_name:Name='None', group_role:AnimGroupRole=Ellipsis, base_pose:PoseLink=\[\], lod_threshold:int=0, alpha:float=0.0, alpha_scale_bias:InputScaleBias=Ellipsis, alpha_bool_blend:InputAlphaBoolBlend=Ellipsis, alpha_curve_name:Name='None', alpha_scale_bias_clamp:InputScaleBiasClamp=Ellipsis, alpha_input_type:AnimAlphaInputType=Ellipsis, alpha_bool_enabled:bool=False)
```


**Bases:** ``AnimNode_BlendSpaceGraphBase``


Allows multiple animations to be blended between based on input parameters

**C++ Source:**

- **Module**: AnimGraphRuntime

- **File**: AnimNode\_RotationOffsetBlendSpaceGraph.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `alpha` (float): [Read-Write] Current strength of the AimOffset

- `alpha_bool_blend` (InputAlphaBoolBlend): [Read-Write]

- `alpha_bool_enabled` (bool): [Read-Write]

- `alpha_curve_name` (Name): [Read-Write]

- `alpha_input_type` (AnimAlphaInputType): [Read-Write]

- `alpha_scale_bias` (InputScaleBias): [Read-Write]

- `alpha_scale_bias_clamp` (InputScaleBiasClamp): [Read-Write]

- `base_pose` (PoseLink): [Read-Write]

- `group_name` (Name): [Read-Write] The group name that we synchronize with (NAME\_None if it is not part of any group). Note that
this is the name of the group used to sync the output of this node - it will not force
syncing of animations contained by it. Animations inside this Blend Space have their own
options for syncing.

- `group_role` (AnimGroupRole): [Read-Write] The role this Blend Space can assume within the group (ignored if GroupName is not set). Note
that this is the role of the output of this node, not of animations contained by it.

- `lod_threshold` (int32): [Read-Write] \* Max LOD that this node is allowed to run
\\* For example if you have LODThreshold to be 2, it will run until LOD 2 (based on 0 index)
\\* when the component LOD becomes 3, it will stop update/evaluate
\\* currently transition would be issue and that has to be re-visited

- `x` (float): [Read-Write] The X coordinate to sample in the blendspace

- `y` (float): [Read-Write] The Y coordinate to sample in the blendspace



---

_property_ `alpha`: float

[Read-Write] Current strength of the AimOffset

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

_property_ `base_pose`: PoseLink

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

- `unreal.AnimNode_RotationOffsetBlendSpaceGraph`
  - `AnimNode_RotationOffsetBlendSpaceGraph`
    - `AnimNode_RotationOffsetBlendSpaceGraph.alpha`
    - `AnimNode_RotationOffsetBlendSpaceGraph.alpha_bool_blend`
    - `AnimNode_RotationOffsetBlendSpaceGraph.alpha_bool_enabled`
    - `AnimNode_RotationOffsetBlendSpaceGraph.alpha_curve_name`
    - `AnimNode_RotationOffsetBlendSpaceGraph.alpha_input_type`
    - `AnimNode_RotationOffsetBlendSpaceGraph.alpha_scale_bias`
    - `AnimNode_RotationOffsetBlendSpaceGraph.alpha_scale_bias_clamp`
    - `AnimNode_RotationOffsetBlendSpaceGraph.base_pose`
    - `AnimNode_RotationOffsetBlendSpaceGraph.lod_threshold`