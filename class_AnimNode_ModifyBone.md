# unreal.AnimNode_ModifyBone

```python
class unreal.AnimNode_ModifyBone(component_pose:ComponentSpacePoseLink=\[\], lod_threshold:int=0, alpha_input_type:AnimAlphaInputType=Ellipsis, alpha_bool_enabled:bool=False, alpha:float=0.0, alpha_scale_bias:InputScaleBias=Ellipsis, alpha_bool_blend:InputAlphaBoolBlend=Ellipsis, alpha_curve_name:Name='None', alpha_scale_bias_clamp:InputScaleBiasClamp=Ellipsis, translation:Vector=Ellipsis, rotation:Rotator=Ellipsis, scale:Vector=Ellipsis)
```


**Bases:** ``AnimNode_SkeletalControlBase``


Simple controller that replaces or adds to the translation/rotation of a single bone.

**C++ Source:**

- **Module**: AnimGraphRuntime

- **File**: AnimNode\_ModifyBone.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `alpha` (float): [Read-Write] Current strength of the skeletal control

- `alpha_bool_blend` (InputAlphaBoolBlend): [Read-Write]

- `alpha_bool_enabled` (bool): [Read-Write]

- `alpha_curve_name` (Name): [Read-Write]

- `alpha_input_type` (AnimAlphaInputType): [Read-Write]

- `alpha_scale_bias` (InputScaleBias): [Read-Write]

- `alpha_scale_bias_clamp` (InputScaleBiasClamp): [Read-Write]

- `bone_to_modify` (BoneReference): [Read-Write] Name of bone to control. This is the main bone chain to modify from. \*

- `component_pose` (ComponentSpacePoseLink): [Read-Write] Input link

- `lod_threshold` (int32): [Read-Write] \* Max LOD that this node is allowed to run
\\* For example if you have LODThreshold to be 2, it will run until LOD 2 (based on 0 index)
\\* when the component LOD becomes 3, it will stop update/evaluate
\\* currently transition would be issue and that has to be re-visited

- `rotation` (Rotator): [Read-Write] New rotation of bone to apply.

- `rotation_mode` (BoneModificationMode): [Read-Write] Whether and how to modify the translation of this bone.

- `rotation_space` (BoneControlSpace): [Read-Write] Reference frame to apply Rotation in.

- `scale` (Vector): [Read-Write] New Scale of bone to apply. This is only worldspace.

- `scale_mode` (BoneModificationMode): [Read-Write] Whether and how to modify the translation of this bone.

- `scale_space` (BoneControlSpace): [Read-Write] Reference frame to apply Scale in.

- `translation` (Vector): [Read-Write] New translation of bone to apply.

- `translation_mode` (BoneModificationMode): [Read-Write] Whether and how to modify the translation of this bone.

- `translation_space` (BoneControlSpace): [Read-Write] Reference frame to apply Translation in.



---

_property_ `rotation`: Rotator

[Read-Write] New rotation of bone to apply.

**Type:**

( Rotator)


---

_property_ `scale`: Vector

[Read-Write] New Scale of bone to apply. This is only worldspace.

**Type:**

( Vector)


---

_property_ `translation`: Vector

[Read-Write] New translation of bone to apply.

**Type:**

( Vector)

### Table of Contents

- `unreal.AnimNode_ModifyBone`
  - `AnimNode_ModifyBone`
    - `AnimNode_ModifyBone.rotation`
    - `AnimNode_ModifyBone.scale`
    - `AnimNode_ModifyBone.translation`