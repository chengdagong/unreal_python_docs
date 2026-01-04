# unreal.AnimNode_HandIKRetargeting

```python
class unreal.AnimNode_HandIKRetargeting(component_pose:ComponentSpacePoseLink=\[\], lod_threshold:int=0, alpha_input_type:AnimAlphaInputType=Ellipsis, alpha_bool_enabled:bool=False, alpha:float=0.0, alpha_scale_bias:InputScaleBias=Ellipsis, alpha_bool_blend:InputAlphaBoolBlend=Ellipsis, alpha_curve_name:Name='None', alpha_scale_bias_clamp:InputScaleBiasClamp=Ellipsis, per_axis_alpha:Vector=Ellipsis, hand_fk_weight:float=0.0)
```


**Bases:** ``AnimNode_SkeletalControlBase``


Node to handle re-targeting of Hand IK bone chain.
It looks at position in Mesh Space of Left and Right FK bones, and moves Left and Right IK bones to those.
based on HandFKWeight. (0 = favor left hand, 1 = favor right hand, 0.5 = equal weight).
This is used so characters of different proportions can handle the same props.

**C++ Source:**

- **Module**: AnimGraphRuntime

- **File**: AnimNode\_HandIKRetargeting.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `alpha` (float): [Read-Write] Current strength of the skeletal control

- `alpha_bool_blend` (InputAlphaBoolBlend): [Read-Write]

- `alpha_bool_enabled` (bool): [Read-Write]

- `alpha_curve_name` (Name): [Read-Write]

- `alpha_input_type` (AnimAlphaInputType): [Read-Write]

- `alpha_scale_bias` (InputScaleBias): [Read-Write]

- `alpha_scale_bias_clamp` (InputScaleBiasClamp): [Read-Write]

- `component_pose` (ComponentSpacePoseLink): [Read-Write] Input link

- `hand_fk_weight` (float): [Read-Write] Which hand to favor. 0.5 is equal weight for both, 1 = right hand, 0 = left hand.

- `ik_bones_to_move` (Array[BoneReference]): [Read-Write] IK Bones to move.

- `left_hand_fk` (BoneReference): [Read-Write] Bone for Left Hand FK

- `left_hand_ik` (BoneReference): [Read-Write] Bone for Left Hand IK

- `lod_threshold` (int32): [Read-Write] \* Max LOD that this node is allowed to run
\\* For example if you have LODThreshold to be 2, it will run until LOD 2 (based on 0 index)
\\* when the component LOD becomes 3, it will stop update/evaluate
\\* currently transition would be issue and that has to be re-visited

- `per_axis_alpha` (Vector): [Read-Write] Alpha values per axis to apply on the resulting retargeting translation

- `right_hand_fk` (BoneReference): [Read-Write] Bone for Right Hand FK

- `right_hand_ik` (BoneReference): [Read-Write] Bone for Right Hand IK



---

_property_ `hand_fk_weight`: float

[Read-Write] Which hand to favor. 0.5 is equal weight for both, 1 = right hand, 0 = left hand.

**Type:**

( float)


---

_property_ `per_axis_alpha`: Vector

[Read-Write] Alpha values per axis to apply on the resulting retargeting translation

**Type:**

( Vector)

### Table of Contents

- `unreal.AnimNode_HandIKRetargeting`
  - `AnimNode_HandIKRetargeting`
    - `AnimNode_HandIKRetargeting.hand_fk_weight`
    - `AnimNode_HandIKRetargeting.per_axis_alpha`