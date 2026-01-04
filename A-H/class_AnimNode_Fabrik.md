# unreal.AnimNode_Fabrik

```python
class unreal.AnimNode_Fabrik(component_pose:ComponentSpacePoseLink=\[\], lod_threshold:int=0, alpha_input_type:AnimAlphaInputType=Ellipsis, alpha_bool_enabled:bool=False, alpha:float=0.0, alpha_scale_bias:InputScaleBias=Ellipsis, alpha_bool_blend:InputAlphaBoolBlend=Ellipsis, alpha_curve_name:Name='None', alpha_scale_bias_clamp:InputScaleBiasClamp=Ellipsis, effector_transform:Transform=Ellipsis)
```


**Bases:** ``AnimNode_SkeletalControlBase``


Controller which implements the FABRIK IK approximation algorithm - see http://www.academia.edu/9165835/FABRIK\_A\_fast\_iterative\_solver\_for\_the\_Inverse\_Kinematics\_problem for details

**C++ Source:**

- **Module**: AnimGraphRuntime

- **File**: AnimNode\_Fabrik.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `alpha` (float): [Read-Write] Current strength of the skeletal control

- `alpha_bool_blend` (InputAlphaBoolBlend): [Read-Write]

- `alpha_bool_enabled` (bool): [Read-Write]

- `alpha_curve_name` (Name): [Read-Write]

- `alpha_input_type` (AnimAlphaInputType): [Read-Write]

- `alpha_scale_bias` (InputScaleBias): [Read-Write]

- `alpha_scale_bias_clamp` (InputScaleBiasClamp): [Read-Write]

- `component_pose` (ComponentSpacePoseLink): [Read-Write] Input link

- `effector_rotation_source` (BoneRotationSource): [Read-Write]

- `effector_target` (BoneSocketTarget): [Read-Write] If EffectorTransformSpace is a bone, this is the bone to use. \*

- `effector_transform` (Transform): [Read-Write] Coordinates for target location of tip bone - if EffectorLocationSpace is bone, this is the offset from Target Bone to use as target location

- `effector_transform_space` (BoneControlSpace): [Read-Write] Reference frame of Effector Transform.

- `enable_debug_draw` (bool): [Read-Write] Toggle drawing of axes to debug joint rotation

- `lod_threshold` (int32): [Read-Write] \* Max LOD that this node is allowed to run
\\* For example if you have LODThreshold to be 2, it will run until LOD 2 (based on 0 index)
\\* when the component LOD becomes 3, it will stop update/evaluate
\\* currently transition would be issue and that has to be re-visited

- `max_iterations` (int32): [Read-Write] Maximum number of iterations allowed, to control performance.

- `precision` (float): [Read-Write] Tolerance for final tip location delta from EffectorLocation

- `root_bone` (BoneReference): [Read-Write] Name of the root bone

- `tip_bone` (BoneReference): [Read-Write] Name of tip bone



---

_property_ `effector_transform`: Transform

[Read-Write] Coordinates for target location of tip bone - if EffectorLocationSpace is bone, this is the offset from Target Bone to use as target location

**Type:**

( Transform)

### Table of Contents

- `unreal.AnimNode_Fabrik`
  - `AnimNode_Fabrik`
    - `AnimNode_Fabrik.effector_transform`