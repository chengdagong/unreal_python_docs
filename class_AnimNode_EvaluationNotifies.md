# unreal.AnimNode_EvaluationNotifies

```python
class unreal.AnimNode_EvaluationNotifies(component_pose:ComponentSpacePoseLink=\[\], lod_threshold:int=0, alpha_input_type:AnimAlphaInputType=Ellipsis, alpha_bool_enabled:bool=False, alpha:float=0.0, alpha_scale_bias:InputScaleBias=Ellipsis, alpha_bool_blend:InputAlphaBoolBlend=Ellipsis, alpha_curve_name:Name='None', alpha_scale_bias_clamp:InputScaleBiasClamp=Ellipsis, current_anim_asset:AnimationAsset=Ellipsis, current_anim_asset_time:float=0.0, current_anim_asset_mirrored:bool=False, mirror_data_table:MirrorDataTable=Ellipsis, named_transforms:None={})
```


**Bases:** ``AnimNode_SkeletalControlBase``


add procedural delta to the root motion attribute

**C++ Source:**

- **Plugin**: EvaluationNotifies

- **Module**: EvaluationNotifiesRuntime

- **File**: AnimNode\_EvaluationNotifies.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `alpha` (float): [Read-Write] Current strength of the skeletal control

- `alpha_bool_blend` (InputAlphaBoolBlend): [Read-Write]

- `alpha_bool_enabled` (bool): [Read-Write]

- `alpha_curve_name` (Name): [Read-Write]

- `alpha_input_type` (AnimAlphaInputType): [Read-Write]

- `alpha_scale_bias` (InputScaleBias): [Read-Write]

- `alpha_scale_bias_clamp` (InputScaleBiasClamp): [Read-Write]

- `component_pose` (ComponentSpacePoseLink): [Read-Write] Input link

- `current_anim_asset` (AnimationAsset): [Read-Write] Animation Asset for incorporating root motion data. If CurrentAnimAsset is set, and the animation has root motion rotation within the TargetTime, then those rotations will be scaled to reach the TargetOrientation

- `current_anim_asset_mirrored` (bool): [Read-Write] Is the current anim asset mirrored

- `current_anim_asset_time` (float): [Read-Write] Current playback time in seconds of the CurrentAnimAsset

- `lod_threshold` (int32): [Read-Write] \* Max LOD that this node is allowed to run
\\* For example if you have LODThreshold to be 2, it will run until LOD 2 (based on 0 index)
\\* when the component LOD becomes 3, it will stop update/evaluate
\\* currently transition would be issue and that has to be re-visited

- `mirror_data_table` (MirrorDataTable): [Read-Write] If bMirrored is set, MirrorDataTable will be used for mirroring the CurrentAnimAsset during prediction

- `named_transforms` (Map[Name, Transform]): [Read-Write] Current playback time in seconds of the CurrentAnimAsset



---

_property_ `current_anim_asset`: AnimationAsset

[Read-Write] Animation Asset for incorporating root motion data. If CurrentAnimAsset is set, and the animation has root motion rotation within the TargetTime, then those rotations will be scaled to reach the TargetOrientation

**Type:**

( AnimationAsset)


---

_property_ `current_anim_asset_mirrored`: bool

[Read-Write] Is the current anim asset mirrored

**Type:**

( bool)


---

_property_ `current_anim_asset_time`: float

[Read-Write] Current playback time in seconds of the CurrentAnimAsset

**Type:**

( float)


---

_property_ `mirror_data_table`: MirrorDataTable

[Read-Write] If bMirrored is set, MirrorDataTable will be used for mirroring the CurrentAnimAsset during prediction

**Type:**

( MirrorDataTable)


---

_property_ `named_transforms`: None

[Read-Write] Current playback time in seconds of the CurrentAnimAsset

**Type:**

( Map\ [Name, Transform])

### Table of Contents

- `unreal.AnimNode_EvaluationNotifies`
  - `AnimNode_EvaluationNotifies`
    - `AnimNode_EvaluationNotifies.current_anim_asset`
    - `AnimNode_EvaluationNotifies.current_anim_asset_mirrored`
    - `AnimNode_EvaluationNotifies.current_anim_asset_time`
    - `AnimNode_EvaluationNotifies.mirror_data_table`
    - `AnimNode_EvaluationNotifies.named_transforms`